---
  title: "The Two Caches of the Mind"
  categories:
    -Blog
  author_profile: false 
  classes: wide
---
I have had so many thoughts on to-do lists over the years.  
  
I was talking to my brother yesterday about how system design and computer architecture has influenced how I think about to-do lists.  
  
First thing is to try to keep the scheduling algorithm simple. But there’s lots of problems that I’ve run into with naive data structures.  
  
I used to try a single priority queue. But even if you try to enforce a fixed size and TTL, you still end up facing starvation, dropping packets, and being unresponsive to messages.  
  
One problem is that importance isn’t fixed. So you need to recompute it once in a while. But this is expensive. If you had to update your posterior distributions and back-propagate residuals on every new data point/piece of information, you’d waste a lot of time on context switches and interrupts.  
  
There’s a time and a place for introspecting and reordering, and a time for executing actions and following orders, and I want to get better at the latter. I’ve been slowly reading decision theory, which is math-heavy, and also psychology for the “emotion management” aspect of productivity, which is more neuro-heavy.

I don’t think most ordinary people need to do these things. But I observe that I struggle with trivial day to day challenges, and if I apply common sense and scientific analysis to my problems, I can live a less demanding life that is equally rewarding.

I’m still trying to figure out how to manage my working memory. The space in my head is low latency, volatile, and low capacity. There’s a lot of cognition that I offload to external structures, but accessing them is slow and runs the risk of distraction, so I want to organize my mind in a way that lets it contains essential information.  
  
What I’m trying out is a hierarchical cache with two layers: the first is for instructions, the second is for habits. The eviction policy on the first one is “least recently used”, and on the second one, it’s “least frequently used”.  
  
Essentially, the problem I want to solve is this: I want fast answers to the question: “what am I doing now?”  
  
Before, this would be really slow, I’d check everything and think a lot. Or it would be super rigid, where I’d get stuck on doing one thing and it would not get done and then nothing got done at all because the pipe got clogged and the production line froze up.  
  
The approach I’m trying is that on some event trigger, I construct the following query: “what do I do in this context?”, but to answer it, I route to the fast path first.    
  
A rigid calendar based schedule only works well when everything is going perfectly with no cost overruns or unexpected tradeoffs/failures. This does not reflect reality.  
  
The alternative is to save thoughts in memory. Let’s say I wake up. Usually I rest in bed for a while in a haze until things become clear. But I want my body to move because movement would get me up to speed faster and my next action will always be the same thing, it’s not something complicated that I need to be thinking about. I don’t need to remember and load everything, just the bare minimum to get me on my feet.  
  
In the morning, the first level cache contains garbage, because I just got up, so normally I’d repopulate it by staring at the ceiling and simulating what the day will be like before getting up. But this is unnecessary. So I go to L2 cache, and since I wake up every day, there is a frequently accessed item labeled “morning routine”, which stores a stack of fixed, predetermined instructions/goals. Even if the cold start to warm state (groggy -> awake) time is the same, I can start doing useful work like brushing my teeth and washing my face earlier.  
  
Is it weird to have to think about this and break it down so explicitly? Maybe. But I am more concerned with how effectively this idea can reduce the molasses and friction of perfectionism under uncertainty. When I apply it to more general scenarios, it tells me to have some cheap heuristics: rules, rituals, routines instead of deriving all behavior from instinct or first principles.  
  
And this means that if I’m confused, I have more options than dropping everything to resolve my confusion. I can instead keep myself grounded by switching to something that I trust to be within the envelope of what I know, what I’ve done before, and can reliably succeed at.  
  
Defaulting to executing good habits is much healthier than going for easy dopamine hits, and often, it can help clarify what to do next when you’re tired and the most powerful mental pathways are too much effort to activate.  
  
You’ll still need them sometimes, but you’ll be able to reserve that for when it’s called for, instead of running out of steam early from overusing the expensive-but-high-quality cognitive circuits.  
  
If I had to summarize all of this: I spend more time thinking about things than I spend doing those things. But my thoughts are valuable, and I need to be careful about where I spend them, especially since excess rumination interferes with executive function. So, wherever possible, I want to think quickly and clearly, getting to the point faster, finishing earlier, and avoiding situations where the value of more knowledge does not exceed the resource cost of acquiring said knowledge. I am underusing the fast-but-less-accurate path, and if I could figure out how to move more traffic to it, it would reduce the heavy load on the slow-but-more-accurate path which is currently acting as a bottleneck to my outputs.
