---
layout: post
title: How should we save the human race?
---

I've been inspired by a number of arguments spawned a post I have made on hackernews to reboot this blog and write this post.

How should we save the human race?
==================================

Ours is the era of doomsday scenarios.
We have found ourselves in a messy place of our development, where we are beginning to understand the many ways we would face extinction level events, without any way to stop them.
I am going to argue that the best solution to increasing the odds of survival is not the save the earth, but rather to get off of it.

## Thinking about the Odds

When building a robust p2p system, we view all the machines involved as fungible interchangeable parts.
In a data-center, seeing dozens of hard-drives failing and machines dieing a day (or even an hour) is a realistic scenario, but in a p2p network (see Mainline DHT) a churn rate (loss and replacement) of 50% to 100% (millions of machines) of computers on the network in a single day is the status quo.


Lets consider a simple passive strategy to ensure the records' survival, making some constant (k) number of extra copies of a file on the network.
Unlike a data-center, almost all methods of failure in a p2p system are independent events.
So we can discuss the likelihood a record is totally lost from the network in terms of:

- Likelihood of total data loss in a single day = Replacement ratio per day ^ number of replicas

- Half life of record = -lg(2) / lg(Replacement ratio per day)

There are some simple conclusions we can draw from this model:

- Unless we re-replicate the record, eventually it WILL be lost

- The expected lifetime of the record increases exponentially with the number of replicas.

Because the number of replicas is an integer (we cannot have a portion of a replica), we can consider the mean lifetime of the record in the system to be:

- (log(number of starting replicas)/log(2) ) * (Half life)

## How does this apply to us?

So,what is our replacement rate?
We really have no idea what the odds are in a day (or any other unit of time) that intelligent life on this planet will die.
However we know of a lot of ways we could go (Asteroid, plague, interstellar zoning issue, gamma ray burst, nuclear holocaust, global warming).
Individually, these may have low odds of occurrence, however we only need one of the uncountable ways for intelligent life on earth to fail.
We can reasonably expect that the likelihood of failure is not dominated by a small set of likelihood methods of failure but rather consists of a great many unlikely methods.
Reasonably, we have more to fear from the failure scenarios we never considered than the ones we have (simply because there are so many of them)

so we know:

- Intelligent life on this planet will cease eventually.
- It is likely happen in a violent and unexpected fashion.
- Attempting to prevent any particular method of destruction will not meaningfully increase our expected survival time.

## Great, so we can't save the world, why bother doing anything?

This discussion is at the core of "taking the long view".
What we learned from the above discussion is that even making colonies would not save us (it would only prolong the inevitable).
The only strategy that ensures survival in the asymptotic sense is constant expansion.
If we ensure that the number of "replicas" for the human race is constant, we have only increased the half life of our species.
Only a net positive rate of expansion of the number independent communities will ensure the asymptotic survival of the species.

## Colonization of space seems a long way off, how could I help?

Terrifyingly, the current state of the art in designing ways for humans to survive off world is still at the level where dilettantes in their garage can help make progress.
You can help by doing and publishing ANY research into the following:

- Closed ecosystems (anything from Biosphere one to some shrimp in a jar)
- Efficient and automated food production (Small scale hydroponics and areoponics)
- Breeding or engineering better suited O2 and food plants
- Automated manufacturing (everything from 3d printers to ore processing)

Another huge problem we are facing is one of short-sightedness in our politics and planning.
While I do not endorse that the "long-view" mentality should be held by any majority you can help by attempting to change public opinion on many issues (just talk to people about it!)

- Space exploration (we could do massive things with a fraction of the war budget)
- Decentralization (robustness goes up with independent communities on earth too, just not as much)
- Valuing the life-quality of our descendants.
- Expansionism (Push the pioneer spirit! Move to underutilized areas and build new comunities!)
