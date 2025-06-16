---
title: 'Innovation under fire'
description: 'How my A-Team at IBM kept our app online during Bluemix outages—and how that innovation under pressure changed my career path.'
pubDate: '29 Mar 2025 11:23:29 GMT'
heroImage: '../../assets/blog-placeholder-2.jpg'
---

OK … so in our last episode, we had the small but mighty A-Team, we had the mission and the executive air cover to create a SaaS portal for IBM’s Tivoli division, and we had made the important but risky decision to build on IBM’s nascent, alpha PaaS Bluemix. This is where having the A-Team really started to pay off.

One of the team members said that we should be able to deploy our app to production many times a day, fully automated, and with no downtime. These days this concept might sound mundane, but for circa-2013 Bill Higgins (and IBM TBH) it was a bit of a revelation. Someone, I think Matt, created a “blue-green deploy” script that would:

1. Deploy a new version of the web app to a random URL
2. Run automated functional verification tests against 1)
3. If they passed, automatically update the CDN to point the real URL at the new app
4. If the app was healthy for an hour, delete the previous instance of the app

Again, mundane by today’s standards but innovative back then (as is the nature of innovation). One problem: Oftentimes Bluemix itself would go down. Our goal was 100% uptime. What were we to do? Well, let me tell you what happened and see if you guess how we did it.

Our web app achieved 100% uptime, even though the alpha version of Bluemix had maybe 98% uptime. Can you guess how we did it? Well, how we did it is a story I’ve never told publicly before, but I think it’s been long enough that I can tell it and not get in trouble. 😅

Someone, I think [Jeff Sloyer](https://www.linkedin.com/in/jeffsloyer/), had the idea that we could dark launch a copy of the web app, which was pretty simple and stateless, also to Heroku, and then our global CDN (I think CloudFlare) would normally route traffic to the Bluemix-hosted app, but if Bluemix was down, it would temporarily route traffic to the Heroku-hosted app. What was funny was that sometimes when Bluemix was down and our app was up, people would ping us and say “How is your app still up?” and we’d say something like “Dunno, must be cached in the Intertubes somehow.”

Anyway, I digress, but my point is that the A-Team was:

1. Innovative
2. Unafraid to take informed risks

Along with “A-Team” these are the next essential elements of strategy, as I would come to understand it.

The project was incredibly stressful and tumultuous, but also incredibly successful and elevated me personally to a next level of eminence in IBM. So much so that I found myself presenting what we’d done to SVP of IBM Software [Robert LeBlanc](https://www.linkedin.com/in/robert-leblanc-0b4b0485/), who said “I really like what you’ve done here. I want you guys to go to Designcamp for Product Teams.” And while I didn’t realize it at the time, that decision by Robert would change my career … for the better. For the MUCH better. That’s the next story … my first experience in large-scale transformation: IBM Design … https://lnkd.in/evUmThrn
