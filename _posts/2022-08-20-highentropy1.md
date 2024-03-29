---
layout: bpost
title:  "Seeking Higher Entropy: Memories [1/3]"
subtitle: "Your brain is a computer, I guess"
permalink: /blog/highentropy1
date:   2022-08-20 21:41:20 -0400
katex: true
category: blog
---

I’ve recently started reading the MIT admission blogs — because those are much more enjoyable to read than the crap drafts of college essays that I write. I’ve just finished reading this [MIT admissions blog post](https://mitadmissions.org/blogs/entry/novelty/), and it resonated with me. In particular, it reminded me of the interactions I have with my friends. So, I decided to write this blog post[^1].

See, I just spent [five weeks of my summer](https://www.mathcamp.org/) at Colby College in Maine, doing math — and other cursed antics — with some amazing people. But five weeks only felt like a short three or two, and upon reading Vincent’s words and thinking a lot, I've come to several conclusions.  

## My brain has an efficient compression algorithm, apparently. 

I’ll just pretend that my brain is a computer, because I understand the latter much more than the former[^2].

> when many memories are similar to each other without anything to distinguish individual ones, each one interferes destructively with the others, so that an attempt to recall any one memory results in a confused recollection of the entire group.

I’m not sure how legit this is, but after some thought, I propose that brains are good at compressing memories. Allow me to (attempt) to explain:

### Math stuff

**Definition 1.** For some random variable \\(X\\), we say the *entropy* of \\(X\\) is some positive real value \\(H(X)\\) that denotes the uncertainty of the value of \\(X\\). 

Basically [[^3]], higher entropy implies that if I tried to guess the value of \\(X\\), then I would be less likely to be correct.

**Definition 2.** For some string \\(s\\), let the *Kolmogorov complexity* \\(K(s)\\) be the length of the shortest description of — or shortest computer program that generates — \\(s\\).

For instance, if we compared K(ababababab) vs K(#oc.b/pj;-), the first string is easily described as “5x‘ab’” whereas the latter is… not easily described. Thus, the first quantity is lower than the latter. 

Entropy and Kolmogorov complexity are inherently related. Namely, the entropy of a random string is related to its Kolmogorov complexity, because if determining some of the characters in the string gives you more information, this means that a computer could reduce the number of cases of the rest of the string based on those characters, thus less Kolmogorov complexity. 

**Example 1.** There are currently on the order of 30000 English words actively being used today. With the standard English alphabet, you can write \\(26^4 + 26^3 + 26^2 + 26 = 475254\\) different strings with four letters or less. Hence, we could literally be using 4 letter words in speech right now, the key idea being that because of the relatively low entropy of English words in use compared to an arbitrary string, we can use less characters for each of those words. For reference, the average length of each word in the paragraph above this one is 5.3 characters. 

### Okay, back on track.

Memories are moments. Ultimately, that means that the entire memory can be described in full in the eye of the beholder in some way. I am fairly sure — but not certain — that this is enough to say that in some way, every memory can be encoded into a string, allowing us to have some analogue of Kolmogorov complexity for a memory. 

Let’s take a memory string, \\(m\\) of a single memory. It is in the brain's best interest to take up the least amount of space possible for each memory, thus, it has to store at least \\(K(m)\\) bits. But is this optimal?

By definition, yes, but in practice, no. 

The discrepancy comes because we store more than a singular memory. For instance, suppose that \\(m_1\\) is the memory of working on school homework, and \\(m_2\\) is a memory of me working on school homework, but the week later. 

\\(m_1\\): Homework session at my desk. Items on my desk: laptop, pencil, paper, glasses case, duct tape. Did Multivar, draft of English essay, chemistry worksheet 2. 

\\(m_2\\): Homework session at my desk. Items on my desk: laptop, pencil, paper, glasses case, duct tape, bag of Doritos. Did Multivar, editing draft of English essay, chemistry worksheet 3. 

The observation is that \\(K(m_1)\\) isn’t much different from \\(K(m_2)\\). However, the brain doesn’t need to store \\(K(m_1) + K(m_2)\\) bits to have both of these memories. 

Instead, the brain can decide to store \\(K(m_1 + m_2)\\), a quantity that takes in a string which is literally the same length as \\(m_1 + m_2\\), but overall does so using much less bits. Instead of having to repeat stuff, the brain can just say “I did the same stuff as in m_1, but with a bag of Doritos, editing instead of drafting, Chem worksheet 3 instead of 2”. 
	
**Theorem 1.** \\(K(a + b) > K(a+c)\\) if \\(a\\) is more similar to \\(c\\) than \\(b\\). 

**Corollary 1.** The brain needs fewer bits to store memories that are similar to each other.

> The days are long but the decades are short. 

Perhaps this is the result of the brain being too good at compressing. High entropy events give our brains lots to process, making the experience seem to go by faster, but the memories are more substantial, because they aren’t just pointers to other locations in memory. Low entropy events are easy to process because they are familiar, and create memories that just end up as pointers to other memories.

**Corollary 2.** Novelty is experiencing high entropy events. 



[^1]: You may have noticed that there are, in fact, three blog posts. I’ve decided to split this into three entries, because I just have so much to say.
[^2]: 2: For the record, I don’t understand computers that much either. 
[^3]: 3: This is not a full description of entropy, I’m only using what I need here. I do, however, recommend learning more about entropy since it’s such an interesting topic. 
