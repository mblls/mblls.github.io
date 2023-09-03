---
title: Learning Software Development on Your Own + Resources
layout: post
---

* TOC
{:toc}


> *Disclaimer* I have a little bit of a long winded intro explaining my special qualifications to create this resource, especially since there are so many other lists out there. That said, these resources I've chosen are _not_ comprehensive, so don't yell at me if you read everything here and don't get a job (actually if that happens email me and I'll share in your dumbfoundedness, because this is a pretty good list).

> Scroll down to Core Fundamentals if you don’t care and just want to get to the good stuff.

# Introduction

My first semester as a Sophomore in college, I was still a nursing major. At that time it was becoming clear to me that I really, really loved my science classes like Anatomy and Organic Chem, but I was really, really hesitant about everything else in nursing. I liked STEM courses in high school, but I didn’t think I’d ever be able to cut it competitively doing a STEM degree in college. Looking back, nursing was _just_ as hard as engineering, so let that be a lesson to never judge a career by its popularity,

One day, I saw [this](https://www.youtube.com/watch?v=ko-KkSmp-Lk) video on interviewing at Google. At that point I, like many other aspiring STEM majors in 2016, was entirely spellbound by the lore of the all-wise, genius developers that worked at Google. I’ve always been a tinkerer, and after seeing this video and hearing all the terminology I didn’t understand (Discrete math? Pathfinding algorithms? Time complexity? Oh my!), my curiosity was piqued. I eventually said “To hell with my insecurities!”, and started looking closer.

I did eventually transfer into an Electrical Engineering program at my university, but I always was tinkering with software, and eventually got a job in it completely outside of my EE degree. As I became more involved in software, I began teaching myself in order to compete with other students coming out of CS programs. Learning online is a double edged sword, for a lot of the information, tutorials, and even sometimes textbooks that you can find are just confusing or straight up misleading.

My goal here is to list all of the really high quality resources I’ve encountered along my journey to self-teach myself computer science. This is by no means a totally comprehensive list, but if you’re starting out from scratch like I was, my hope is that this will guide you in the correct direction.

# Core Fundamentals

[Learning How To Learn](https://www.coursera.org/learn/learning-how-to-learn) [Free, Online Course] - Start here. Seriously, don’t skip it.

Software engineering is endlessly broad and ever expanding. It’s very easy to feel overwhelmed on where to start because there’s always so much noise about the latest and greatest language, weird niche ML concepts, or processor architecture, all of which aren’t super useful for the beginner. These things can also tend to be trends, whereby their relevance comes and goes. I spent way too much time worrying about trends when I was starting out, instead of learning the core fundamentals. If you start here, I promise you’ll have a good foundation for anything you encounter later.

If you don’t know a programming language yet, I recommend choosing Python, and then picking between C++, or Java. Why? Python has very readable syntax and a well-supported community. IMO, it’s a cheat-code for getting into software (and for interviewing, but that’s another story). I recommend choosing C++ or Java as a supplemental language because they’re also well supported, still used everywhere, and they expose you to some of the fundamentals of working with computers that other languages can abstract away from you (plus they are a little more “robust” than Python alone, but the details on that aren’t important for this stage).

Most of the resources are free and online.  

[Google's SWE Book](https://abseil.io/resources/swe-book) [Online Textbook] - This book is fairly non-technical, and it will expose you to some amazing ideas used at Google for maintaining quality SWE culture. It’s a good thing to be exposed to early on, and to then reference often.

[The Odin Project](https://www.theodinproject.com/) [Self-Study Course] - Google engineers are at it again, making insanely useful resources for the rest of us. This will get you off of the ground if you’ve never coded a thing in your life. It includes exclusively free resources that take you from total N00B to a genuine tinkerer. If you’re wondering where to start, start here.

[Learning Python the Hard Way](https://www.amazon.com/dp/0134692888/ref=emc_b_5_t) [Textbook] - This is a great first coding book to get your feet wet and expose you to a language and the command line. It doesn't get too in-depth, and will be a good litmus test to see whether this whole programming thing is right for you. This book would be well supplemented with [https://realpython.com/](https://realpython.com/).

[MIT 6.006 Introduction to Algorithms, Fall 2011](https://www.youtube.com/watch?v=HtSuA80QTyo&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb) [Online Course]- Once you start getting a feel for a language and start doing some coding questions, I recommend you start watching this series. It guides you through the basic algorithms you’ll see in interviews and your day-to-day life. You can skip the proofs for now (unless you find them helpful), you just need to understand the core algorithms, their applications, and their time and space complexities. This course is aimed at all undergraduate students, but Algorithm courses tend to have more of a research angle to them. Bonus points if you implement the algorithms yourself (and you should)!

[Operating Systems: Three Easy Pieces](https://pages.cs.wisc.edu/~remzi/OSTEP/) [Online Textbook] - Single handedly the most important resource in this entire list. Getting familiar with Operating Systems exposes you to real Software Engineering. This book assumes some basic C knowledge, but don’t let that deter you, as it’s worth learning in any case. If you find this book interesting (and the homeworks), then you have a blooming career as a software engineer ahead of you.

[Computer Networks: A Systems Approach](https://book.systemsapproach.org/) [Online Textbook] - A really good overview for networking. This book can get fairly dense, but once you’ve mastered some of the fundamentals, the question you’ll likely ask yourself is: “How do computers talk to each other?” This text will help you understand the IP suite, and some common networking protocols.

[Programming Principles and Practice Using C++](http://www.nylxs.com/docs/Programming__Principles_and_Practice_Using%20C++%20(Cpp%20Cplusplus).pdf) [Online Textbook] - Not only a great beginner-friendly tour of C++ (written by the author of the language no less), this book gives fantastic advice on good software engineering practices. This is where’d I start if you want to learn C++

[Effective Java](https://kea.nu/files/textbooks/new/Effective%20Java%20%282017%2C%20Addison-Wesley%29.pdf) [Online Textbook]- More great resources if you’re just starting out and needing to choose a language.

# Advanced Resources

[Deadlock Empire](http://deadlockempire.github.io/) [Online Game] - Once you’ve finished reading about concurrency in OSTEP, use this online game to test your knowledge of how a Scheduler can break with concurrency.

[Use The Index, Luke!](https://use-the-index-luke.com/) [Instructional Website] - A must read for optimizing SQL queries (and for understanding indexes, as well)!

[Computer Science 186, 001 - Spring 2015](https://archive.org/details/ucberkeley-webcast-PL-XXv-cvA_iBVK2QzAV-R7NMA1ZkaiR2y?tab=collection) [Online Course] - DB architecture. This stuff is very dense, but the instructor is a wiz. I recommend pursuing this course from beginning to end to get a high level overview of how DB work, but I wouldn’t sweat all of the details, especially if you’re just starting.


[Distributed Systems Course - Dr. Martin Kleppmann](https://www.youtube.com/watch?v=UEAMfLPZZhE) - Dr. Martin Kleppmann is a foundational CS communicator, and this course proves that out further. If you need an intro into distributed systems, this is an absolutely phenomenal resource.


# Coding Practice

You're going to have to do a coding interview one day if you want to work in software, so might as well get started now!

[https://leetcode.com](https://leetcode.com)

[https://projecteuler.net/archives](https://projecteuler.net/archives)

[https://www.hackerrank.com/dashboard](https://www.hackerrank.com/dashboard)


# Tech Blogs

I recommend perusing the following links with the mentality of learning how to communicate software ideas well. Sometimes the posts can be super advanced, and other times they're a little dry, but a lot of times (especially Julia Evans blog) these can be invaluable resources for learning new topics.

[https://jvns.ca/](https://jvns.ca/)

[http://www.paulgraham.com/](http://www.paulgraham.com/)

[https://rachelbythebay.com/w/](https://rachelbythebay.com/w/)

[https://dropbox.tech/](https://dropbox.tech/)

[https://netflixtechblog.com/](https://netflixtechblog.com/)

[https://otoro.net/ml/](https://otoro.net/ml/)


# Other Resources

These are just things I personally like, take it or leave it.

[https://bikeshed.com/](https://bikeshed.com/)

[The Coding Train](https://www.youtube.com/channel/UCvjgXvBlbQiydffZU7m1_aw) - A great introduction to graphical programming led by a very enthusiastic instructor.

[A Pattern Language](https://www.patternlanguage.com/) - Ever heard of the "Gang of Four" and their software design principles book? Well, this is where they got their ideas for _that_. This is a super cool website to supplement the book which explores how to design things for humans. 

[Thinking Fast and Slow - Daniel Kahneman](https://www.amazon.com/Thinking-Fast-Slow-Daniel-Kahneman/dp/0374533555)


# YouTube Channels

These are some extra resources to add a little CS spice into your YouTube subscriptions.

[https://www.youtube.com/@numberphile](https://www.youtube.com/@numberphile)

[https://www.youtube.com/@Computerphile](https://www.youtube.com/@Computerphile)

[https://www.youtube.com/@Vihart](https://www.youtube.com/@Vihart)

[https://www.youtube.com/@BenEater](https://www.youtube.com/@BenEater)
