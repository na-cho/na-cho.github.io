---
layout: post
title: "Dad Jokes are Just Nim"
description: "This shouldn't exist."
comments: false
keywords: "Nim, Game Theory"
---

The following is adapted from my AoPS Blog. 

If you don't understand any terminology here, it's probably in [here](https://na-cho.github.io/files/nim.pdf).

**Definition 1**: Let us define a *dadjoke* to be a turn in which a person responds to a string of letters \\(a\\) containing the substring "im", where spaces, punctuation, and capitalization are ignored by choosing an occurence of "im" in \\(a\\), and then removing everything before the occurrence and then concatenating the resulting string to the string "hi". 

Example: A dadjoke on the string "I might cry" would be "hi ight cry". Spaces are included in the response for readability. 

Now, suppose two people, named A and B, are conversing in an isolated universe. Person B tells person A a string, and then they take turns dadjoking the string, starting with player A, until a player cannot dadjoke anymore, in which case the last person to make a dadjoke wins the battle of wits. 

Example: With an initial string of "I'm imitating you"
Player A: "Hi imitating you"
Player B: "Hi itating you"
Player A: "Darn." (Player B wins and Player A is sad)

Note that this game is guaranteed to be impartial:
 - The number of occurrences of the character "m" must be strictly decreasing with every dadjoke
 - The rest of the requirements are quite obvious. 

Thus, by Sprague-Grundy, the dadjoke is isomorphic to Nim. But we can do a bit better than that.

The obvious observation here is that any character that is not an "i" or "m" does not matter, except for separation of these special characters. Furthermore, any occurence of "ximx" where "x" represents non special characters, can be interpreted as a "single stone" on a larger pile. 

Example: Consider the string "Nim is cool, I'm simply minimally interested." Note that this is directly isomorphic to a game of single pile nim with 4 rocks on the pile. 

The issue occurs when we have a string like "ximmx", where one "m" is dadjokable but the other is not (at least, not directly).

It is well known that normal single pile nim is a N game as long as there are a nonzero number of objects in the pile. We can interpret this as dadjoking the last “im” in the string. 

Let a string in the form “imm..mm” be a \\(n\\)-block, where \\(n\\) is the number of adjacent “m”s. For instance, “im immature” has a 1-block and a 2-block. 

**Claim:** A conversation is a \\(P\\) game (first person who dadjokes loses) iff there are no odd blocks in the string. 

**Proof:**
If all blocks are even, then the "strategy stealing" argument works: dadjoking on a certain \\(n\\)-block where \\(n\\) is even gives the next player a \\(n-1\\) block and a bunch of even blocks, where then they can make it a \\(n-2\\) block and even blocks, and now all blocks are even once more. This guarantees that the second player always has a valid move, no matter what the first player dadjokes. 

If there exists an odd block, then take the last odd block, and dadjoke it: now it’s an even block, followed by only even blocks, which by earlier means that the second player cannot win. 

Next up on conversational Game Theory: Losing strategy for the game ("I lost the game," in laymans).
