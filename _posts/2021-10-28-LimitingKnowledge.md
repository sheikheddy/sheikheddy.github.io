---
  title: "Limiting knowledge"
  categories:
    -Blog
  author_profile: false 
  classes: wide
---
The project I'm working on is so large, so complex, and so old that our institutional knowledge about it is fragmented across the minds of the dozens – even hundreds – of engineers that built it. And even if you had an incredible machine that could eat all of those people’s brains and perfectly extract everything they know about the codebase into a book, there’d still be missing pages in places where nobody understands the full picture of the components and how they interact. And even the pages that you could read would be impossible to decipher: dense, jumbled into a mess with no coherent structure, and so long that you’d have no hope of getting through it if you ever wanted to get anything else done.
That doesn’t mean that nobody has tried. We can redefine the problem. Make it slightly less impossible than “comprehending the totality of the system”. How about this:
Given a human H who has a finite learning time T, we can define a routine R such that R(H, T) = K, where K is the knowledge that human H gains after being subject to R from time 0 to time T.
R can be any combination of activities. Watching recordings, reading books, writing emails, browsing documentation, talking to people, diving into the code, making small changes. What matters is that each activity has a cost associated with it (time) and benefit (knowledge).
Let’s fix K’ to be our goal: the smallest possible subset of knowledge that stills contain enough information to let us complete our tasks. If we know less than K’, we are underinformed, and if we know more than K’, we learned things that were not relevant/applicable/useful. We can also fix H, since in this scenario H is the human (or Haozhang) who we need to teach/train.
Now we’ve reduced our analysis to two variables: R (the routine we use to learn K’) and T (the time it takes to learn K’).
Observe that T depends on R. If we change R, we either increase or decrease T. For example, if we selected R to be “doing nothing at all”, then T could be unbounded.
In contrast, we can imagine some optimal R’, a perfect learning routine that minimizes T so we can learn what we need to know as fast as possible.
Let’s rearrange our original equation to make this easier to visualize. We can claim that R(H, K) = T. In other words: a routine that gives a human some knowledge K will take time T to complete.
Hence, we informally define R’ to be the best R. Formally, for all possible values of R, and with fixed H, K’; R’(H, K’) <= R(H, K’).
That was a mouthful: All we’re saying is that following our personal R’ will teach us K’ in the shortest time possible. For completeness, let’s name that shortest time, and call it T’.
I think about this a lot
In practice, K’ is often unknown, so we usually try to ensure that K’ < K. We’re okay with learning a little extra, and not knowing enough is considered bad.
And in practice, we don’t know for sure that following any R will yield K in time T, all of this is stochastic and probabilistic. We always have constraints that shrink the space of available R.
Often, the size of K' is... actually pretty small, and R' is impossible to reach. There will always be an infinitesimal more point of efficiency to extract.
What we usually do is pick a random R and start exploring, and then experiment with making tiny tweaks to R, and record whether we increased or decreased T significantly.
The realization is that you are always following R, even when you're not following R (perhaps especially then!).
if you're frozen by indecision and overthinking and researching the options without doing anything, you should consider whether that R will reduce T more than the alternative of just doing something, picking a direction and iterating in spite of the uncertainty.
there are constraints that restrict your feasible R. but how close do you think your R is to R'? I think mine isn't even on the same planet.
I’ve carefully avoided using any calculus, but if you’ve studied applied mathematics or classical mechanics, this is similar to using the Euler-Lagrange equation of the calculus of variations to find the function R’ that minimizes the functional mapping the function R(H, K’) to the scalar T.
Don’t run away! I promise I'll give you a concrete example.
# Deciding which recordings to watch
This has a certain cost, easy to calculate, but how much of the increase in K intersects with your K'?
You can predict the future. You can estimate what information is contained in a resource before going through it. Your assumptions may be flawed, incomplete, but your instincts generally point you in the right direction.
Embrace that there will always be gaps, and you cannot eliminate every last one. Make strategic steps. Perfectionism kills.
Think about it from the perspective of the people creating the lectures. They have no idea what will be the K' of every person attending.
They can't design for the union of all K's, no way that would fit into their T.
And chances are they're not thinking about it that formally either. They just think, "oh, this was useful for me, it might be useful for them, learning more is always better than learning less, right"? But that's wrong. You can get stuck in tutorials forever without making any impact.
Learn as little as you can possibly get away with to do what you want. Sometimes that will take you into deep dives into compilers, programming languages, distributed systems, system design & architecture. Sometimes that will take you to copy-pasting from stackoverflow.
You do need deep understanding sometimes, superficial education is dangerous. Knowing "why" can and should be part of K'.
But for work, what I've seen rewarded is raw speed. Once I'm done, I go learn for its own sake as a fun enriching activity, and I don't confuse that with the sort of learning I do when the situation is: "I need to do something, how? Who can I ask for help?"
If you are efficient, you are done for the day in 4 hours, and you go outside and exercise and watch netflix or play games or meet people or read books. Your effective rate of pay is increased. if you are inefficient, the work doesn't go away, you just take longer to do it, and you have to sacrifice evenings and weekends just to keep up.
The problem isn't distractions or slacking off. It's that we should put a bigger multiplier on the hours we're already putting in.
