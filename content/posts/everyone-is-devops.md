---
title: "Everyone Is A Devops Now"
date: 2021-07-01T20:18:58-04:00
draft: false
---

I’d argue if your users are not contributing to automation of the infrastructure and cloud services, they care the most than you are a sys admin in disguise.  

I’ve been frequently in a situation when a developer or data engineer would approach me and ask me for help with the automation of some complex workflow with cloud services I’ve never used before. After looking at the diagram I usually give them a deal – I teach them how to automate their solution in the cloud, but they’d have to do it over a GitHub repository following our best DevOps practices while I and other DevOps engineers are involved in the PR reviews of their code.

I haven’t met a single person that has refused this offer. Without ceremony we jump next on ensuring their working environment supports Infra-as-code (IaC) tools and services. Sadly, MS Windows is still a bit of a challenge for some of them, but things are rapidly improving on this front with the introduction of WSL2. 

Engaging users works well in start-ups where it is an absolute necessity, you might be the single DevOps supporting ever growing cloud infra, but this approach is also applicable in large organizations like John Wiley & Sons, my current employer with infra spread globally across different cloud providers.

So, how do you recruit DevOps from the ranks of your users? It usually follows this pattern:
1.	Talk to everyone, anytime and anywhere.
I’ve stopped counting the number of projects I’ve started just by talking to people by the coffee machine or while going together for a casual jog during a lunch break.
2.	Teach them git and explain them that Git is all you need to know
3.	Find a real project – or risk forgetting everything you’ve learned.
4.	Rinse and repeat

## Talk to everyone, anytime and anywhere
Besides being a good listener, after all we are trying to solve real problems, be ready to explain complex concepts on the back of a napkin on a small notice. 

I’ve done countless presentations about Kubernetes to groups and individuals who’d contact me because someone I knew sent them my way. Sometimes that meant I dropped other things I was working on to give them the info they needed to understand if Kubernetes would be a good fit for their use case. I find those interactions very rewarding even on a personal level regardless of the outcome. I get in touch with great individuals with whom I might collaborate in the future if not immediately. 

## Git is all you need to know

Depending on the users’ experience with Git we spend some time on Git workflows and what that means in terms of collaboration and releasing changes to different environments. If there is one message newbies should take home is the importance of using Git and branching strategies when collaborating with others over the Internet. Everything else follows out of this and it is easy to automate once it is managed in some source code repository.

Some of the users have been so good at this I’ve told them if they ever plan to change career tracks, they should consider joining some of our DevOps team. The education goes both ways. Users learn something about DevOps best practices, and at the same time DevOps learn first-hand about the intricacies of the infra and services they are expected to support in the future.

Others needed more time to absorb the differences between GitHub and Git, but once that chasm was bridged, they were off to the races and started contributing and innovating. 

There are no stupid questions and show empathy for the awkward first steps of your users. Learn by failing and don’t be afraid to fail.

## Find a real project 

Working on a real project is one of the skin-in-the-game factors that increases the chances of success of engagement tremendously. I’ve seen too often people forget everything they’ve learned in some online course for the simple reason they never apply the newly acquired knowledge to their projects.

More importantly no training covers challenges encountered in real-life projects. These challenges prompt discussions whose outcome is always the refinement of the architecture of the infrastructure to the satisfaction of all involved.

My role here is to really educate and guide users, answer their questions, and address their concerns. I look over their shoulder and perform PR reviews. They do all of the work. 

Initially the biggest obstacles to engaging others as DevOps come from the security team. All those unknown users are potential security threats to them. The answer to their concern is developing a trust in the process by providing total transparency, granting least privileged access to resources, performing reviews, auditing users’ actions, separating code from secrets, scanning code for vulnerabilities, and good monitoring and alerting. 

The Sec team realizes fast, ok maybe not so fast , that it’s in their best interest to educate users in best security practices instead of managing Sec Groups manually over protracted periods of time. Users always find a way to get what they want but that might create sec holes in order to circumvent the block standing in their way. Not to mention they’ll consider you an annoyance that needs to be avoided at any cost.

## Rinse and repeat

Once empowered users usually come back with new projects, start contributing with new modules, or fix your issues you never had time to fix yourself 

## An example of a successful DevOps transformation

A seasoned DBA engineer, yes DBA is still a thing but we are converting them fast to DevOps, had no previous knowledge of Git but he understood the importance of automation in the cloud. In the first month we’ve covered a Git, collaboration over GitHub and using Terraform for IaC automation.

In the second month this person has identified and applied alone an Open Source Terraform project for provisioning Couchbase clusters in AWS, which he contributed to the common DevOps infra GitHub repository. 

This success inspired him so much that he is now working on managing databases in Kubernetes with Operators, which is our next chapter in conquering Kubernetes.
 