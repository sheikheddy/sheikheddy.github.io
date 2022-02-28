---
  title: "6,124,890 Page Visits in 6 months: where all my time goes and why I don't get anything done."
  categories:
    -Blog
  author_profile: false 
  classes: wide
---


**TL;DR: Page reads are inefficient (many unnecessary network calls)**

**Problem** *My output is too slow at work.*

**How slow should I be?** *3x to 10x faster than I am.*

**How did I come to that number?** *Read below.*

## Measurement 

### Sources 
- Browser extension "Webtime tracker" from [Peta Sittek](https://www.petasittek.com/) 
- Browser extension [Time Tracker](https://chrome.google.com/webstore/detail/time-tracker/mokmnbikneoaenmckfmgjgjimphfojkd) 
- [BrowsingHistoryView - View browsing history of your Web browsers](https://www.nirsoft.net/utils/browsing_history_view.html) 
- [Azure DevOps REST API](https://docs.microsoft.com/en-us/rest/api/azure/devops/wit/?view=azure-devops-rest-6.0) 
- git shortlog --subject --name --commiter --since="" --before="" -- . [Stack Overflow](https://stackoverflow.com/questions/31190474/how-to-count-git-commits-per-user-in-a-date-range) 
- Microsoft Viva Insights (MyAnalytics)
- [OutlookStatView Show statistics / report for Outlook mailbox](https://www.nirsoft.net/utils/outlook_statistics.html) 
- Teams activity analytics (only for **Jan and Feb 2022**)
- Daily journal notes in [Obsidian](https://obsidian.md/)
- Weekly status reports

## Caveats
- The interval of dates examined for browser data:
	- Begin: 2021-08-24 (August 24 2021)
	- End: 2022-02-27. (February 27 2022)
- For privacy reasons, raw browser data cannot be shared.
- Three daily journal entries were not recorded due to travelling. 
	- These dates were (2022-11-26, 2022-11-27, 2022-11-28)
- Vacation and other time off: 6 weeks, so this is ~20 work weeks.
- I started at Microsoft on 2021-04-12, but the first 19 weeks of browser data were wiped when I reformatted my work laptop in an attempt to fix a troublesome bug. 
	- Browser data was not backed up in OneDrive, and I could not keep local copies due to compliance restrictions.
- Again: **teams activity analytics are only available for Jan and Feb**

## Observations

### Browser 
- **6124980** page visits
- **81680** unique webpages
- **2707** unique websites
- **4408901** active seconds (approx 6.5 hours daily, including weekends)
- <mark><b>36%</b> of my time is being spent outside my top 15 sites</mark>
 ![](/assets/images/otherlongtail.png)

### Communication
- **3322** Teams messages sent in **Jan and Feb**
![](/assets/images/teamsjanfeb.png)
- **45 hours** sharing audio/screen in **Jan and Feb**
- **413** sent emails
	- **April to August** account for **182** (36.4/month)
	- **September to November** account for **161** (53.7/month)
	- **December** accounts for **15** (on vacation)
	- **Jan and Feb** account for **55** (27.5/month)
![](/assets/images/emailcounts.png)
- **Rank 61** out of **16000+** participants in MS Elite (an internal early adoption + bug reporting platform)
	- This should not count for much. Most teams were aware of the issues I pointed out and were already planning to fix them. It's difficult to say if my feedback made any difference at all.
	- Also, I intentionally selected surveys to optimize for points, which goes against the spirit of the competition. Really, the main takeaway is that I had a lot of free time. ![](/assets/images/mselite.png)


### Obsidian Notes
- **12665** non-blank lines
- **205** markdown files
- **255** screenshots
- **156411** words

### Code
- **32** Pull requests checked in/under review
	- **September to November** accounts for **7**
	- **December** accounts for 0 (on vacation)
	- **Jan and Feb** account for **25**
- **9** Pull requests abandoned
	- **September to November** accounts for **8** 
	- **Jan and Feb** account for **1**
- **6** Spam rule rollouts
	- **September to November** accounts for **0**
	- **Jan and Feb** account for **6**
- **50th percentile** for all time commits to codebase
	- **September to November** rank is at **0th** percentile
		- Maybe not literally 0th percentile, but the commits I did make were not useful and had no impact, so I'm not counting them.
	- **Jan and Feb** rank is at **84th** percentile
		- You'll have to take my word that I did not artificially inflate commits to game this measurement. I did not expect this result.
		- There may of course be problems in my methodology. Maybe this only means I need to squash and amend my commits more.

### Tasks
- **20** work items assigned 
	- **April to August** account for **1**
	- **September to November** account for **4** 
	- **Jan and Feb** account for **15**

<mark>I have completed 10x fewer tasks than the average for software engineers at my level in my org</mark>


## Reasoning (and fixes)

Jan and Feb have been better than September to November. I switched teams to a new project and manager, and changes to personal circumstances also mean that I am in better health. But there's still a lot of room for improvement.

### Mistake 1: Extraneous fetching
I was underestimating how much time was going into the "other" category, mostly because on any given day it wouldn't form a majority of the pie, so I didn't know it was bigger than my top 5 sites put together.

![](/assets/images/othertypical.png)

This meant that I had an incomplete understanding of the full picture, and my improvement plans were made with incorrect assumptions about where my time was going. For example, I used a content blocker called [News Feed Eradicator](https://chrome.google.com/webstore/detail/news-feed-eradicator/fjcldmjmjhkklehbacihaiopjklihlgg) to significantly cut down time on Youtube, but the absolute savings were only marginal.

![](/assets/images/youtubereduction.png)

Looking into the 2707 websites, a clear pattern emerges: most of these are technical articles, documentation, or blog posts. 

I'm reminded of a [Paul Graham quote: "The most dangerous way to lose time is not to spend it having fun, but to spend it doing fake work."](http://www.paulgraham.com/selfindulgence.html)

It's easy to _feel_ productive when reading about something that is tangentially related to your work. The issue is that it is unlikely that aimless wandering will get you any closer to solving your problem.

Once, one of my friends invited me to play a video game with her, and I prepared by reading and watching endless strategy guides and tutorials and practicing aimlabs. But when we actually entered a match, I made dumb mistakes that even very new players quickly learned to avoid. I would have done far better if I just _played the game_ instead of overcomplicating it. 

<mark>Passive content consumption is not the same thing as thinking.</mark>

### Mistake 2: Chatty I/O

I already knew that emails were negatively correlated with productivity, but thought that mine were an exception, and they clearly aren't.

My most productive month by far was December, when I was on vacation and only did necessary administrative emails in batches.

Emails produce a permanently running thread in your brain's resource pool. Your default action during any quiet period becomes to open your inbox and stare at it even if there isn't anything new, just so you can respond quickly if there is.

I sometimes observe people who will open social media on their phone and scroll and tap every few minutes, and I always feel bad for them, because being constantly online left less time for them to think and reflect and be in the moment. 

But I was doing the same thing with emails on my laptop! Making inbox rules to stuff distribution lists into folders is not sufficient. The classic advice is that since answering emails is a necessary evil, you should reserve a slot for it on your calendar, and not touch your inbox outside of that timebox. I'll do that for inbound emails.

What about outbound emails? 

Those are even worse. If you're responding to too many emails, the engagement creates more engagement, and that feedback loop means you can notice that the process is too heavy and kill it.

But when you're the one sending emails, the amount of time you can potentially waste is limited only by the size of your audience multiplied by how long it takes to read your message. 

Few people are nice enough to tell you, "hey, you are broadcasting to too many people, and the content is only relevant to a tiny proportion, consider reducing how much notification spam you're producing". 

I thought adding people to threads was considerate, since otherwise they wouldn't have access to the discussion, and that creates information silos.

But silos aren't so bad. This is perhaps one of my most controversial opinions. Here's how I would explain it to me from last year:

Small teams are great in many ways and routinely outperform large ones. There's a sense in which this is a function of the size of the team itself, rather than the "average quality" of the individual members. 

Think about how you'd evaluate the design of two different distributed systems. In "small teams", each node usually only talks to its neighbors, and in "big teams", every node has to synchronize with every other node. The number of edges in a complete graph with $n$  vertices is $\frac{n(n-1)}{n}$ , and the number of all distinct paths between any pair of vertices will grow on the order of n factorial.

Factorials!!!!! That will be a nightmare.

When does it make sense to send an email to more than the bare minimum number of recipients? 

Existential threats and major incidents. There, the usual peer-to-peer propagation is too slow, so we need a centralized authority to force push some critical update instantly to all globally running instances. 

Oh god, that sentence gives me anxiety. I hadn't really thought about how much damage my emails were doing, and looking at my outbox I feel like most of these are really more appropriate for an issue tracker or a forum instead.

Yes, emails are more likely to get responses, but it's for the same reason that sending someone a text that says "911! Call me NOW!" is likely to get a response. I'll think carefully about whether it is really appropriate to reach for email as my first choice of channel for communication.

### Mistake 3: Blaming the build systems (this section can be skipped)

I was overestimating how much the package restore and project compilation steps were contributing to overall development time.

Once, I was going over a 2 to 4 hour recording I'd made of me fixing a minor bug. Watching myself code is a special form of torture, but programmers are all closet masochists, so it's okay. 

What was not okay was the jarring flow-breaking sensation of everything grinding to a halt every time I needed to get dependencies. The time I spent staring at the screen waiting for the target binaries to be ready viscerally _felt_ like it was being wasted.

I got my hands on some build telemetry data, and then checked to see how much of my time was actually spent on compilation. 

What I found was that over the week spanning 2022-02-10 to 2022-02-17, I had spent a grand total of *38 minutes and 35 seconds* on compilation. I didn't believe it at first, but the local build logs hadn't been cleared from my machine yet, and they matched up with the telemetry, and for my sanity I decided not to look into whether or not the logs were lying. 

Instead, I decided, "of course, the problem was never compilation, which is CPU bound, but downloading packages, which is network I/O bound, and therefore much slower". 

All that was left was to prove it. I knew the number of package files I had on disk, I knew how much storage they were taking up, but I couldn't do much about that. 

I mean, I could try to remove unnecessary dependencies, but that'd be tedious and lame. Even if it worked, it'd be a temporary solution, only lasting till the bloat built up again. I declared that the true villain was the low rate of data transfer (throughput) of the cache servers. 

I tried improving the performance of the package downloads. I don't think I really had a clear idea in mind, and I don't know why I didn't just plug an ethernet cable into my dock, but here's what I can make out from my half-illegible notes.

My thesis was basically that the designers of the package download architecture could not have anticipated the rampant abuse of it today. Piling one sloppy assumption over another, I made up my story for why speed would be neglected.

As the codebase grew, we kept adding more and more packages, and the current maintainers have to keep it from buckling under the weight. So all the initial assumptions from back then about load patterns will be wrong now, and all the work being done on it nowadays will be more focused on scaling to more concurrent users and keeping some minimum level of uptime. 

A hobbyist might have a decent shot at helping out by finding some slow part and making it faster. Maybe we could swap out the compression algorithm used before the packets are sent out based on the pattern of files to be sent over or something, I dunno, I'd know it when I saw it. 

In fact, I did not know it when I saw it. The whole thing was actually pretty boring. There was a jumble of messy version handling, and then it deferred all the interesting parts to nuget. 

The natural next step would be to try to optimize nuget, but I had already made a misguided attempt at that around the same time I'd gotten it into my head that I should profile/debug [dotnet/runtime](https://github.com/dotnet/runtime) and figure out how it did LOH allocations and change that to be "less bad".

That was also around the time I cold emailed someone who had written some cool posts about how the microsoft build engine worked asking for how to get started on contributing to this one part of MSBuild which I'd discovered didn't work too well for our codebase, and after a short exchange over a few days I sent him a code snippet diff with some extremely stupid change X. 

He replied, "Are you suggesting we do X? Definitely would lead to really bad race conditions. This is not something I will entertain".

Ah, I must have cried myself to sleep that night. I mean, that was totally the correct response, X would have been a total disaster, I was just crying because I sucked so much that I didn't even consider it before he pointed it out, and because I knew I was never going to be good enough to actually get a patch into MSBuild.

But I'm a closet masochist, so it's fine :)

The thing is, I have standards, I want to at least be an *effective* loser. I had spent weeks going down this rabbit hole, but I'd never even calculated how much time I expected to save!

14 hours, 13 minutes, and 18 seconds. That was how much time I'd spent waiting for the dependency file copy to finish during Jan and Feb. I'd spent more time than that reading about the CLR!!

Look, I'd be the last person to discourage learning about cool stuff and trying to save other people time, but I had to admit one thing: I was doing it for myself, not for my job. Every single time someone asked me to do something, I took on a wayyy harder version of the problem than what they'd assigned to me, and in a way that was kind of selfish (or at least self-indulgent).

I could do the easy version first. I was actively making a choice every time I went neck deep into the weeds. This was just the latest in a long set of wild goose chases. At the time, I thought the challenge was the best way to become better and have more impact. Now... I'm not so sure. Doing easy work, but lots of it really really fast, I think maybe that'd get me closer to getting a patch into MSBuild eventually than the crap I was doing earlier. 

And as an added perk, my boss will be happier too. I made some decent improvements to my performance in the last two months, and I think I can do even better by reading less and actually more solving problems instead of just repeatedly failing at them. 

### Cliches I'll keep in mind
- Focus on acquiring hands-on experience with a rapid feedback loop. The economics of writing means that popular text is usually only suitable for a broad audience. History does not define the future.
	- Experts in a field already know most of what the books can tell them. Further growth comes by learning directly from reality.
- You can spend a lot of time planning and still have huge gaps in your mental models. It's good to be careful, but we have a review process for a reason, find the right balance between quality and velocity.
	- Explore vs exploit is a classic tradeoff. Set exploration limits. 
- Don't try to read the whole internet at once. You'll be too slow! Filter for relevance, quality, and efficiency. Prune open tabs. Focus. You often only need a tiny amount of information to achieve your goal. 
	- A query to the right person can answer your question faster and more accurately than randomly guessing with the search engine. Your time is not _infinitely_ less valuable than theirs.
- Mechanical skill does matter.
	- But you can get very far with easier investments into decision making, teamwork, and monitoring. 
- Prioritize one thing at a time.
---





