# A Better Tomorrow

[Unsplash Image Credit: Spencer Watson ](https://unsplash.com/photos/raz0rm8WJwg)

# A Better Tomorrow

As an independent consultant, I lead technical teams and move the needle for modernization in enterprises. I keep coming back to the idea of what the project looks like for a new team member. What is the architecture? How are pull requests done? What technologies are we using? What tech stack do they want to move towards? 

When I join a new team, I ask the most important question: How do we deliver software to our users? The answer tells me what I need to know about the team and often the organization. Often times, I hear we don't have a DevOps person to do the CI/CD. As a result, deployment is ad hoc and "hand-crafted". No two deployments look the same. And there is a single person tasked with releasing. 

For the teams where there is little to no idea of DevOps, which for me is a mindset or principle, I start simple. I introduce a build tool, dependency management, and other goodness. Often, there is push back against spending time on things like automation and tests. As a lead, you have to balance the time spent with shipping features. 

Features? Yes, what we deliver to the users so they can receive value and in my case do there job in an enterprise setting. Here it is, your moment of Zen: The act of shipping features in a reliable way is the most important feature of all.

## Features vs How We Ship Features

I love Hong Kong action movies. Often the movies take principles of honor and loyalty and pit them against each other. I sense this conflict at many organizations I visit. They want to ship many features to the users and neglect how to do so in a standard way with quality. Why does this happen? A new button on the application that everyone can see is more tangible than automated builds. Leadership needs to understand the cultural shift to DevOps. But, changing an organization's culture is a story for another day. This is a slice of my view on enabling teams to deliver quality software often.

## Everyone Ships

More often than not, I end up working on automation for a team, because it is important. Also, many times folks are waiting for a DevOps person to do it. Serious. I even named an antipattern of one person "doing" DevOps after myself, DaveOps&trade;. If you are waiting for someone to come to your team and "do" DevOps, bad news. A single person doesn't scale. I view projects even before I start them with the understanding that I am going to leave one day.

With this mindset, I set out to make sure the entire team is better without me. Deployments. Everyone knows how we deploy. Tester? Analyst? Manager? It doesn't matter. I start with creating a checklist for how we deploy. I ask folks to contribute to it and keep it up to date. To make this happen I usually have to get the builds automated enough. Enough for folks to run a script or press the button in our CI/CD tool. Part of the deployment checklist includes details of what we are deploying, features. This may include links to JIRA tickets, test script results, CI links. It always includes notes for post deployment. If the unexpected happened that prevented a successful deployment like a production database is down, disk space issue, etc. we want to know. That way we can come back and fix it later and prevent it from happening. Or safeguard against it. Each checklist serves as a log of past deployments. What did we deploy 3 months ago on Friday? (You can deploy on Friday, if you are ready) I can't remember what I did last week, which why we document deployments. We rotate deployments responsibilities.  Everyone deploys. I am here to support you. So is the rest of the team. When everyone deploys, everyone gets comfortable at deploying and it becomes normal. In the future, consider continuous deployments. (There is a sequel to this post)

## Who Loves You and Who Do You Love?

When deploying, know who depends on your app and services. Let the teams know ahead of time, communicate. More important, know who you depend on. Document any APIs, databases, etc. that your team depends on. Run pre deployment tests on dependencies. If a service is down that your team needs, should you deploy?

## Please Welcome...

After a team has automation, and deployments are boring. All good right? Well, a new developer is starting, they can deploy fine but they are asking questions about the tech stack. Point them to the architectural design records. Don't have one? Good place to start [Homepage of the ADR GitHub organization](https://adr.github.io/). Architectural Design Records (ADR) answer why a certain technical path was taken and or why it was changed. Most of all it gives context. It serves as a history of technical decisions and increases the teams understanding. Remember you may not be on the team one day. Often I have seen new developers come to a team and change the tech stack and problems arise. They didn't have the context on why a path was chosen and we can't blame them. I blame us. We gave them no context on the architectural decisions. Architecture diagrams are helpful for understanding as well. Concepts like ADR give more context even to those who have been on the team for awhile. I find myself in conversations with others wondering why we went down a particular path. It is nice to pull up an ADR and see the reasoning. For example, we chose Go for the CLI because in our spikes it performed well and developers can pick it up quickly. Or for the rules engine we rolled our own and wrote in Clojure for the reasons a, b, and c. ADRs also ensure you justify decisions. We are not doing Resume Driven Development (RDD) are we? (A practice where you pick popular frameworks technologies for your resume)

## The Past is the Past

ADRs are great for documenting the past. What about where the team wants to go in the future. As soon as you build something you discover a better way to build it. Once your code is in production and users are engaging with it you see ways to improve. You hear about a new approach that you can use or a new technology that can make things faster. Or your team has a better understanding of the problem. My favorite reason to change the tech stack is to simplify. What is the least amount of technology we can use to solve the problem. Serverless? Write these ideas and assumptions and how they will help the team. Pick some and try them out. We can call this Architecture Futures or a roadmap with different paths. 

## Please README

"Just look at the code". I have heard that many places...100K lines of code will tell you all you need to know. Eventually. A great README can jump start a new developer on the team. It should contain how to run the code, tests etc. How to contribute, related links to JIRA etc.. Everything a developer needs to get started. Keep it up to date.

## Last Day 

If my whole team, can deploy with automated builds, document design decisions (and future ones) we are in good shape. If onboarding is an easy task because the README for each repo is well done and up to date. Well, I feel comfortable saying goodbye.

The less a team needs me in delivering quality software often the more easy I can leave. I focus on what makes a team better at delivery so that we can focus on our core responsibilities.

## Be Brave

None of what I mentioned are considered features and often there is a pushback against working on them. And yes you cause friction with your team or organizon pushing for building roads when they want to build cars. It is a balance. Kaizen - continuous improvement. These non features sometimes are done in the shadows with no story points assigned. Your project's automation and DevOps mindset is a silent guardian against failed deployments. Less fear of Friday deployments. Less pages in the middle of a dark night.

Start today.

