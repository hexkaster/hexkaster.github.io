---
title: "Three Certs in Six Months, Notes from My 2025 Cybersecurity Year"
date: 2026-01-15 000:00:00 +0800
categories: [cybersec]
tags: [cybersec]
image: /assets/img/motoko.png
---

## I. Foreword
This is not a regular post, in the sense that I could just sit here, write a long recap of the certs I took this year, and move on with my day. This one leans more toward a mix of rant, personal update, storytelling, and a How The Certs Went™ type of breakdown. If you want to skip the warmup and go straight to the [meat and potatoes](#iii-2025-certs---crto-osep-and-cpts), feel free. 
## II. Introduction
As I started writing this, I kept thinking about how 2025 has probably been the closest I’ve ever gotten to what people like to call an [_annum mirabilis_](https://arxiv.org/pdf/2112.13519). At the beginning of the year, I got a little obsessed with that idea, and looking back, it feels slightly misplaced. Not wrong exactly, just overdetermined.

It wasn’t flawless. There were stretches where things felt heavy and constrained, especially physically. I ended up dealing with my second case of De Quervain’s tendonitis, this time in my right hand instead of the left. I had already gone through a milder version of it in 2024, but this flare-up was more persistent. Around April, several things shifted at once, including a job change and the growing realization that surgery would probably be unavoidable. Knowing there was a clear path forward helped settle my head more than I expected.

De Quervain’s is simple on paper. Certain tendons get inflamed, they swell, the swelling causes more friction, and the whole thing feeds back into itself. For most people, rest solves it. I learned the hard way that I’m part of a small minority who have extra tendons in each hand, which makes conservative treatment basically useless. Surgery was the only real solution. I had my left hand done in October 2024 and the right one in July 2025, which meant I spent close to a full year unable to sit down and grind labs or certs for long stretches. That only really changed in late August.

Once I felt functional again, I tested the waters by jumping into [HTB Pro Labs](https://www.hackthebox.com/hacker/pro-labs). I ended up finishing Dante, Zephyr, and about two thirds of Offshore before my one month license ran out, all while having surgery scheduled for the following week. That was enough to convince me I was back.

After recovery, I went all in. I rested for a couple of weeks post surgery, then jumped straight into Zero Point Security’s [CRTO](https://www.zeropointsecurity.co.uk/course/red-team-ops). I spent just under three weeks on the material, booked the exam, and passed. Right after that, I picked up OffSec’s [OSEP](https://www.offsec.com/courses/pen-300/), studied for a bit under two months, scheduled the exam, and passed with seventeen flags. Then, by late December, I decided to take on HTB’s [CPTS](https://academy.hackthebox.com/preview/certifications/htb-certified-penetration-testing-specialist), which went more or less as expected. Success.

## III. 2025 Certs - CRTO, OSEP and CPTS
### CRTO
![[/assets/img/CRTOI.png]]

First of all, props to [**Rastamouse**](https://x.com/_RastaMouse) for CRTO. This is probably my favorite certification course so far, and that’s not something I say lightly. It hits a very rare sweet spot. It’s _technically solid without being suffocating_, and it’s actually fun to work through, which is something most certs completely fail at. It explains things that are often hand-waved away, like the [Early Bird attack](https://digital.nhs.uk/cyber-alerts/2018/cc-2282), but it does so without turning the course into a theoretical dissertation. You feel like you’re learning real tradecraft, not memorizing trivia for an exam.

What really stood out to me is how intentional the course feels. The content sits somewhere between HTB’s CAPE and OffSec’s OSEP, but it avoids the worst tendencies of both. It doesn’t lean too hard on CAPE’s quirks or gotchas, and it doesn’t do the OffSec thing where you’re thrown into the deep end and told to “figure it out” as if confusion were a teaching methodology. CRTO respects your time. Every topic feels like it’s there for a reason, and every lab feels like it’s reinforcing something concrete rather than just flexing difficulty.

A big part of that comes down to how the material is explained. **Rasta** has this professor-like clarity that’s surprisingly rare in offensive security training. He doesn’t rush, but he also doesn’t ramble. You can tell he understands not just the what, but the why, and more importantly, the how people actually get lost when learning this stuff. It feels like being taught by someone who has both done the work and taught it enough times to know where students usually trip.

The course itself walks through genuinely advanced Active Directory exploitation techniques. Delegation attacks, cross-domain trust abuse, weird MSSQL privilege escalation paths, things that don’t always show up neatly in beginner or even intermediate material. On top of that, it introduces shellcode creation, modification, and usage in a way that’s approachable without being dumbed down. Yes, the shellcode work is scoped to Cobalt Strike, but honestly, that’s fine. It gives you a mental model and a foundation, which is what matters. Once you understand the mechanics, the tooling becomes interchangeable.

I’d gladly take the course again, and I already plan on tackling CRTO II in 2026. Easy recommendation.

> Below are some of the materials, scripts, and other resources I used to prepare for the exam:

**A quick note on scope:**  
CRTO is very self-contained, and that’s one of its biggest strengths. If you already understand the basics of network pentesting and Active Directory, the course material alone is more than enough to prepare you for both the exam and real-world use. You don’t need to pile on external labs or side resources to "fill gaps." Everything you need is there, clearly explained and intentionally sequenced, which makes the learning experience feel focused instead of scattered.

| Study Resources       | Review                                                                                                                                   |
| --------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| CRTO Course Materials | Do all of it. Seriously. The course is tightly scoped and every section matters. Skipping parts here will come back to bite you later.   |
| CRTO Course Labs      | Mandatory. This is where the course really clicks. Don’t just grab the flag, understand why the attack works and how you could adapt it. |

### OSEP
Now, shifting gears to OSEP.

This one is funny to talk about because people love to oversell it as some mythical, ultra-advanced rite of passage, when in reality it is exactly what OffSec says it is. An experienced pentester course that teaches you how to break into more complex environments. No more, no less. And to be fair, it actually delivers on that promise.

If CRTO feels like a well-structured, guided tour through AD abuse and C2 operations, OSEP feels like being dropped in the woods with a compass and told to make it back before sunrise. Not in a cruel way, but in that very particular OffSec way where the learning curve is very much __your problem__. The material is there, the labs are there, but nobody is holding your hand or reassuring you that you’re on the right track. You either adapt or you sit there staring at Kali at 3 a.m. wondering where things went sideways.

The course leans heavily into evasion and bypassing defensive controls. AV evasion, AMSI bypasses, process injection, custom loaders, application whitelisting tricks, network filtering bypasses, all the good stuff. You spend a lot of time writing or modifying your own tooling, and whether that feels empowering or miserable depends entirely on how stubborn you are about doing things your own way. Some days it feels great to see your loader finally work. Other days you wonder why you didn’t just pick a quieter hobby.

They also cover client-side attacks, phishing-style payload delivery, Linux post-exploitation, SQL Server lateral movement, credential abuse, and a decent chunk of Active Directory internals. None of this is groundbreaking in isolation. If you’ve been around for a while, you’ve probably seen most of these concepts before. Where OSEP shines is in forcing you to chain them together in a real, messy environment where nothing lines up cleanly and nothing is written for you.

I'd say that what really separates OSEP from most post-OSCP courses is the __exam__. Instead of isolated machines or neatly scoped flags, you’re dropped into a network where everything is connected and nothing is obvious. You break in, stay quiet, pivot, escalate, dump credentials, move again, pivot again, and just keep going until you run out of ideas or energy. It forces you to think like an operator rather than a student solving challenges, and that’s where its real value lives.

I spent a bit under two months studying, booked the exam, and walked out with __seventeen flags__. The exam itself was **smoother than I expected**, mostly because the course had already pushed me to build enough custom tooling to handle whatever the environment threw at me. I didn’t get the _secret.txt_ flag, even though I knew exactly where it was and still had almost a full day of lab time left. At that point it wasn’t about skill, it was about effort, and I was honestly ready to be done. I missed my girlfriend, had a couple of personal things to take care of, and decided that was enough.

Would I recommend it? __Yes__, with a very specific caveat. You need to actually enjoy problem-solving under pressure. If you go in expecting something linear or guided like CRTO, you’ll hate it. If you want a course that forces you to tie everything together and sit with uncertainty for long stretches, it’s great.

Would I take it again? __Hard to say__. In terms of quality, it’s on par with CRTO. In terms of cost, it’s a different universe. CRTO cost me a little under 250 euros thanks to PPP, _living in Brazil occasionally has its perks_. OSEP, on the other hand, came in at a staggering __1,750 dollars__. It’s not worth that much in any objective sense, but OffSec will keep being OffSec for the foreseeable future, so I did the math and decided it was acceptable. I’m pretty cheap, I don’t care much about luxury or status purchases, and the money was already there. Still, it’s hard to look someone in the eye and say any certification is worth 1,750 dollars. Everyone just values things differently.

> Below are some of the materials, scripts, and other resources I used to prepare for the exam:

| Study Resources                              | Review                                                                                                                                                                                                                                                                                                                                    |
| -------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| OSEP Course Materials and Extra Miles        | Do pretty much all of them. I really can’t stress this enough. The value of the course lives in the details, and skipping sections comes back to bite you later.                                                                                                                                                                          |
| Course Challenges                            | Same advice here. Do all of them. They force you to actually internalize the techniques instead of just skimming the concepts.                                                                                                                                                                                                            |
| HTB: Dante, HTB: Zephyr, HTB: Offshore       | Great for getting comfortable with large networks, AD attacks, and longer attack chains. These are much more CTF-like than the actual exam, but still very much worth the time.                                                                                                                                                           |
| VulnLab Shinra and VulnLab Wutai             | I didn’t use these personally, but pretty much everyone I trust says they help a lot with exam preparation, so **I think they’re worth mentioning**. Also, they’re a bargain for what you get.                                                                                                                                                        |
| [Extravenger's OSEP Playground Repo](https://github.com/Extravenger/OSEPlayground) | This repo has almost every script you’d ever need to pass. My script-writing was a bit rusty, so I initially used it as a reference, but do not just copy things blindly. I spent a few hours understanding the logic behind the bypasses and then rewrote everything from scratch. As reference material, though, this is absolute gold. |



### CPTS
CPTS was the last cert I wrapped up this year, and honestly, it felt more like checking off a box than hitting a major milestone. Not in a bad way, just in a very matter-of-fact one. I already had an HTB Gold subscription from last 2024's Christmas discount, which I originally bought with the intention of taking [CAPE](https://academy.hackthebox.com/preview/certifications/htb-certified-active-directory-pentesting-expert). I even finished the CAPE course, but CPTS ended up being the more logical next step, so I pushed the CAPE exam further down the line.

Because Gold lets you see the answers for every exercise, I didn’t feel any real need to grind through the entire CPTS course from scratch. That might sound lazy, but it was more about honesty than shortcuts. I already knew most of the material well enough to explain it to someone else, so forcing myself to rediscover it line by line would’ve been performative more than educational.

The content itself is solid. It’s dense, structured, and full of genuinely useful material for anyone who’s still getting their footing in offensive security. If you’re early in your journey, CPTS is excellent. But if you already have experience, a lot of it feels like revision rather than discovery. Familiar attack paths, familiar enumeration logic, familiar mental models. So I spent a day or two filling in the exercises with what I already knew, sanity-checked a few things, and moved on.

What did frustrate me a bit is HTB’s requirement that you complete the entire course before you’re even allowed to schedule the exam. I still don’t really understand why that constraint exists. It feels more bureaucratic than pedagogical, especially when the exam itself is perfectly capable of testing whether you actually know the material. But, cest la vie. You play the game in front of you.

> Just to be clear, none of this is meant as a knock against CPTS. I’d still absolutely recommend it to anyone who wants a strong foundation in network-based offensive security. It does exactly what it sets out to do, and it does it well. It’s also refreshingly reasonable in its exam format. Ten days, no webcam paranoia, no weird performative proctoring rituals. **Compared to OffSec’s insistence on keeping a camera on at all times, which is still one of the strangest exam experiences I’ve ever had, CPTS feels almost humane**. Sitting there smoking in front of a webcam while someone watches you hack is not a vibe I'm exactly eager to relive.

By late December, pretty much everyone I knew was thinking about taking CPTS anyway, so it felt like the right moment. Shoutout to **jaogler** btw. Shared momentum helps more than people like to admit.

In the end, CPTS delivered what it needed to deliver. **I took the exam, passed, closed the tab, and moved on w/ my life**.

> Below are some of the materials, scripts, and other resources I used to prepare for the exam:

| Study Resources                        | Review                                                                                                                                                                                                  |
| -------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CPTS Course Materials                  | Solid and comprehensive. Excellent for building foundations, though more experienced practitioners will recognize much of it as revision rather than new material.                                      |
| HTB: Dante, HTB: Zephyr, HTB: Offshore | Useful for getting comfortable with larger networks and longer attack chains. The exam feels roughly on par with Offshore in difficulty, though some people compare it more closely to Dante or Zephyr. |
| Prior Real-World or Lab Experience     | **Easily the biggest factor**. If you’ve done network pentests or similar labs before, the exam will feel fairly straightforward. I know it's kinda douchy to put this in as a **study resource**, but I really DO feel that even the slightest contact with real world corporative pentesting will give you a big edge in this exam.                                                                           |

Now, on to OSED, or OSWE, or CRTO II, whatever. I'll spend the next couple of weeks playing videogames and that's it.
## IV. Reflections on the Year

This was not an _annum mirabilis_, and honestly, it probably shouldn’t have been. Life isn’t perfect all the time, and it’s a bit silly to expect it to be. Something beautiful is always going to happen, something frustrating or messy too, and that mix is what makes it interesting in the first place.

The year started out fine. I liked my job and the people, but the routine was exhausting. Long commutes, waking up at 7 a.m., going to sleep at 1 a.m., constantly running around. Not unhappiness, exactly, just this persistent "meh" hovering over everything. Looking back, it really wasn’t as bad as it felt at the time. [We focus too much on the leaf instead of the tree](https://mariejudith.medium.com/theres-a-saying-that-everything-you-need-in-life-is-available-to-you-right-now-in-your-current-f42a00b10ccf).

Still, **it wasn’t great**. In April I switched to a remote job, and that *completely shifted my perspective*. For the first time in a while, I could actually structure my days in a way that worked for me. Suddenly I had time for the things I’d been neglecting. Studying languages, reading books, training at the gym, traveling with friends and family. Space to breathe and enjoy life outside the routine. I **love** security research, and now I get to do it at my own pace. Grind certs at my own pace. Do CTFs with friends at my own pace. It rocks :).

I also ended up traveling more than I expected. São Paulo, then Guarujá for client stuff, Goiânia, back to São Paulo again. After that, New York, a quick three day trip that happened to line up with a Bladee show. Seeing him live was surreal, and the trip itself sat in that nice overlap between work and just being around interesting people, which does a lot more for your head than you realize.

Argentina came next, for Ekoparty. I reconnected with some friends from my old job and finally met a bunch of people I had only known as usernames and profile pictures. [C3l3S14N](https://x.com/c3l3si4n), [pr3y](https://github.com/pr3y), [luska](https://x.com/LuskaBol/), 0dallen, dur4ndal, and the whole [Marcio Herobrine](https://marcio.club/) crew. Sharp, funny, genuinely great people. Being there reminded me how much community matters, especially the kind where you can talk shop without having to explain yourself every two sentences.

For the last couple of years, most of my offsec conversations happened at home. My saint of a girlfriend never minded. She listens to my ramblings with the maximum amount of interest a person can reasonably sustain while having no idea what I am talking about. Still, there is only so much hacking, CVEs, and shellcode enthusiasm one person should have to absorb. Having more people to share that energy with again felt grounding, and probably healthier for the ecosystem as a whole.

All that said, I am lucky. Not the "random money falling from the sky" kind of lucky, but the quieter kind that comes from a mix of circumstance and effort. **I am, admittedly, a beneficiary of a lot of undeserved good fortune**. Being born to supportive parents, with enough stability to take risks without everything collapsing underneath me. None of that is earned, and pretending otherwise feels dishonest. At the same time, I do not think my luck is entirely passive. Some things are completely out of your control, but others only happen because you **sharpen your chances**. You show up, you learn, you talk to people. You put yourself in environments where interesting things tend to happen. Most of the time, nothing comes of it. And then, one day, **something does**.

**Connecting with people quietly raise the probability of something good happening**. You talk to someone without a goal in mind, exchange a few half formed thoughts, and move on. Nothing seems to come of it at the time. Then, months later, something clicks. A problem shows up that reminds you of a conversation you barely remember having. A name surfaces when an opportunity appears. An idea you dismissed as vague suddenly has context and weight. *The connection was already there*, just waiting for the right moment to make sense. It feels nice.

## V. Sinbad the Sailor

We’ll get a bit off track here, but honestly, I don’t see another way to wrap this up.

Long story short, now that I finally have free time like I haven’t in the past two years, I’ve thrown myself into reading everything I could get my hands on, from technical papers to autobiographies to classic literature. A few months ago, I was wandering through a bookstore that recently opened in my neighborhood with my girlfriend, and there I picked up [_The Idiot_](https://ia601708.us.archive.org/31/items/idiot00whisgoog/idiot00whisgoog.pdf), [_Crime and Punishment_](https://archive.org/details/crimepunishment00dostiala/page/22/mode/2up) (which I’ve yet to read in English, since I already read it in Portuguese and want to try a more internationally respected edition), and [_The Count of Monte Cristo_](https://dn790001.ca.archive.org/0/items/countofmontecris01duma/countofmontecris01duma.pdf), which I just finished. I have this habit of hyper-fixating on whatever catches my attention for a stretch of time, and December ended up being marked by that obsession with this book, specifically.

> I WARNED YOU THAT THIS WOULD GET OFF-TRACK

Part of what kept pulling me back to _The Count of Monte Cristo_ had nothing to do with plot mechanics or clever twists, but with how **unashamedly patient the book is**. Modern storytelling feels anxious; it wants to justify itself quickly, move fast and prove relevance. Dumas does the opposite. He lets years pass... He lets plans sit untouched. Silence sometimes does most of the narrative work. There are entire stretches where nothing explodes, nothing is revealed, and yet the tension grows precisely because time is being taken seriously. Time is not just a backdrop here, it is a force, almost a character, grinding people down or quietly rearranging their lives.

That makes sense once you remember how Dumas was writing. This wasn’t a **neat, self-contained novel dropped onto a shelf**. It was serialized, published in chunks, meant to be lived with week after week (I've jokingly said that it was their equivalent of One Piece). The structure reflects that. Characters disappear for hundreds of pages and return altered, like old acquaintances you run into years later and barely recognize. Reading it now, in a **world optimized for constant stimulation, feels oddly rebellious**. It asks you to slow down and trust that payoff does not need to be immediate to be real.

There’s also something very 19th century about how seriously the book takes ideas. Not in an academic sense, but in a lived one. Concepts like honor, fate, patience, loyalty, debt, gratitude, they are not themes to be dissected, they are forces that shape how people act. Even Providence, which sounds archaic now, is treated less like a religious abstraction and more like a way of making sense of chaos. A framework for understanding why suffering exists without collapsing into nihilism. You don’t have to believe in it literally to feel its pull. It functions psychologically precisely because gives structure to uncertainty.


> “You mistake,” he said, “Providence does exist, only you have never seen him, because the child of God is as invisible as the parent. You have seen nothing that resembles him, because he works by secret springs, and moves by hidden ways. All I can do for you is to make you one of the agents of that Providence.”

And maybe that’s why it stuck with me. **I am not particularly romantic about the past, and I don’t think history had better answers than we do**. But I do think we’ve lost *some* comfort with the idea that life unfolds according to rhythms we do not control or fully understand. We want dashboards, metrics, guarantees. Dumas offers something softer and stranger. The suggestion that **events accumulate meaning over time**, that delay is _not_ failure, that waiting can itself be an active stance toward the world (provided your heart and actions are correctly aligned).

I also couldn’t help thinking about Dumas himself. A wildly prolific writer, constantly working, constantly in debt, constantly producing. He wrote like someone who trusted momentum more than perfection. There’s a generosity to that. The book is messy in places, indulgent in others, occasionally absurd, and yet completely alive. You feel the author’s confidence that if he keeps moving forward, something worthwhile will emerge. That feels human in a way that overly polished modern writing sometimes doesn’t. If anything, it's about endurance. About how _long arcs matter_. About how identity is shaped less by singular moments than by sustained attention and patience. About how reading a very old, very long book can recalibrate your sense of time in a way that quietly seeps into the rest of your life.

"Wait and hope" (the book's biggest takeaway) sounds naive until you realize **how hard both of those things actually are**, especially when life isn’t dramatic enough to feel tragic, but not fulfilling enough to feel complete either. I think that’s why it felt reassuring to me, especially looking back at this past year. Stretches of life that feel flat, repetitive, or vaguely unsatisfying are not failures, they are just part of the accumulation. That waiting is not wasted time. That some things only make sense once you finally have the space to notice what they were preparing you for.

Thanks for reading!
