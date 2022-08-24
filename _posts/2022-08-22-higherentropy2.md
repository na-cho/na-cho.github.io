---
layout: bpost
title:  "Seeking Higher Entropy: Experiences [2/3]"
subtitle: "Having to solve optimization problems in the first place is suboptimal."
permalink: /blog/highentropy2
date:   2022-08-22 21:41:20 -0400
katex: true
category: blog
---
## [Exploration vs. Exploitation](https://en.wikipedia.org/wiki/Multi-armed_bandit)

With the goal of experiencing Canada/USA Mathcamp to the fullest, I actively thought about optimizing happiness during the five short weeks I was there. 

In essence, with finite time and many, many ways to experience an event, there are two different things one can do:
- **Explore** new activities or people, and seeing how happiness they yield, then
- **Exploiting** the ones that you find make you happiest. In other words, sticking with the groups of people and activities you like best.
My initial approach to this problem was the solution to another problem, but in hindsight, this was suboptimal.

## Why the 37% rule fails. 

In essence, [I had already seen this problem before](https://en.wikipedia.org/wiki/Secretary_problem), and I knew the solution. After attempting to apply the 37 percent rule, here’s some things I observed:
- The people I ended up hanging around were approximately the people I hung around on the first day, but the people I became close with weren’t people I was hanging around a lot at the beginning. Success?
- Activities? A completely different story.  

See, in the first week of Mathcamp, I had played approximately 1200 games of [Castlefall](https://www.bpchen.com/castlefall/rules.html). Maybe too much, but justifiable so, because it’s a great game. However, we almost completely stopped after two-ish weeks.
The problem was that we started playing the game in a super low entropy way. The number of new clues per game eventually went to zero, even if we were using different wordlists. 
I’m not sure about the others, but after the games became consistently low entropy, I stopped playing. 

**Claim 1.** The happiness yield for an activity decreases if it has low entropy. 

In a way, this result [shouldn’t be too surprising](https://en.wikipedia.org/wiki/Diminishing_returns). Once something becomes entirely predictable, the experience has extremely low Kolmogorov complexity. 

However, this means that I would probably not enjoy spending the 63% of my time exploiting the maximal activity found during the other 37%. Meaning, that it would not be optimal to apply the 37% rule. 

The problem is now harder to solve, since we can’t just reduce it down to finding a near optimal activity in a short period of time. The solution I used from that point on was basically “do whatever you like doing that you aren’t bored of,” since I was too busy having fun to think about optimization problems. I was satisfied with camp despite not having addressed activities at all [[^1]].

I propose a better solution: exploiting while exploring. Namely, if you continue to do what you enjoy, but with minor variation, then the experience is already somewhat different and thus entropy is not as low. Applying this to something that you have found yields high amounts of happiness should theoretically extend its longevity. 

This solution has some problems, yes. For instance, entropy is still concerningly low when the activities are similar to each other. 

I still think it’s at least closer to optimal with low effort, because it
- abuses the fact that activities that are similar to each other have similar happiness yields[[^2]],
- makes an experience you enjoy more memorable, by Corollary 1, and
- addresses diminishing returns.

In a way, this is a conservative way of approaching novelty, but with a smaller \\(\Delta\\), so that you have a safer bound on \\(\Delta \cdot \nabla_{\overrightarrow v}f\\), where \\(\overrightarrow v\\) is the way you introduce variance, and \\(f\\) is the happiness function at the original activity you enjoy. 

**Claim 2.** Experiencing novelty in smaller ways can still yield high amounts of happiness.

Perhaps this is the compromise for the “separating [of] the moments” that Vincent desires and the routine-based lifestyles many of us build:
living a standard day with a twist, approaching old things in new ways. 



[^1]: 1: Maybe the real Canada/USA Mathcamp was the friends we made along the way. 
[^2]: 2: Namely, one can think of this as finding a [local maximum](https://en.wikipedia.org/wiki/Gradient_descent)
