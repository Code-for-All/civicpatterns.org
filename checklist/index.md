---
layout: default
title: Civic Software Checklist
---

Civic Software Checklist
========================

A growing number of civil society organisations and news organisations
produce software. This document collects tips to tackle two common
challenges they face:

* **Sharing your code** with others in such a way that it actually invites
  collaboration, rather than just 'token' open source code.

* Reducing the **risk from contractors** that work on a project for some
  time and then move on to other clients. It's important that the code
  they leave behind can be understood and extended by others. 

Both issues can be addressed by following the (mostly non-technical)
strategies laid out here.

**Note:** This is a collaborative document. Please feel free to submit
pull requests to suggest changes. The goal of this document is to be as
concise and understandable as possible. If you see any fluff, help cut it
away!


## Engaging in open source development

* Avoid **not invented here** syndrome. Another group may have already
  solved the problem you're dealing with, so spend some time on
  research. If their solution looks overly complex, think twice: while
  this may be a sign of bad code, it could also be an indicator that
  their project is mature and has learned to deal with many different
  concerns. 
 
* It's usually **cheaper to adapt than to re-build**. Your idea is probably
  special to you, but experience shows that starting a new project has a 
  fixed cost that will eat up a significant part of your budget.

* When you release code, think about **separating tools from projects**.
  For example, in a crowd-sourcing effort, you might want to separate
  the mechanism you use to collect data (e.g. text messages) from the
  code that is specific to the topic of your project (e.g. potholes).

* Keep your code up to date. You might want to surprise the world with
  a big, new feature sometimes, but that should not be a reason to stop
  sharing your code until that new thing is done. Big, infrequent
  updates kill collaboration.

* When people announce their intention to contribute to your project,
  invite them to submit some code as early as possible. Save discussions
  on product design and general strategy for later.

* When people contribute, try to include their changes, even if they're
  not on your roadmap. Take time to review the code, and if it needs
  improvement, guide contributors through making the necessary changes.


## Checklist for starting a project

* **An open source license**. Explicitly defining the terms of re-use is
  the key to opening your software. Never write your own licenses, but
  instead use either the GPL or an MIT/BSD license ([here's a comparison](http://choosealicense.com)), and place the chosen text in a 
  file called ``LICENSE``.
 
* **Set up a public code repository**. Code sharing platforms like
  GitHub enable developers to work together easily. They improve your
  internal development workflow as well.
 
* **A ``README`` file.** This introduces a user to your code base and should
  answer basic questions: what does your project do? What different
  components are there, how do they fit together? How would do you
  install the software? What would a typical workflow look like? How
  can people contact you, report errors or contribute to the project?
  
  The ``README`` is the first place where potential contributors will 
  learn about your project. It is not a piece of advertising or a 
  donor-facing document. Invest some time in having it proof-read
  by technical people who don't know your project.

* **Detailed installation instructions.** Most web platforms aren't easy
  to install, and many of the intricacies of setting up your project may
  fall out of the scope of the ``README`` file. Make sure you provide 
  detailed instructions on what other software is required to run your
  project and steps to take in a separate ``INSTALL.md`` file.
  
  To further simplify the installation of your project, you might want
  to provide support for [docker.io](http://docs.docker.io/reference/builder/)
  or [Vagrant](http://www.vagrantup.com/). Both tools isolate a piece of
  software in its own virtual computer.
  
* **An issue tracker.** This not only lets users report problems, but
  it also creates a publicly visible list of what features you are 
  planning and what problems you already know about. If you're using
  GitHub, every repository has its own issue tracker set up automaticaly.
  
  Make sure you keep your issues up to date, and written in English. To
  help potential contributors, mark issues which are easy to tackle and
  well-contained with a special tag or label. If someone offers to
  contribute, you can point them at these **low-hanging fruit**.

* **Mailing lists.** Set up a mailing list for developers, and invite 
  anyone who is contributing code to subscribe to that list and join the
  discussion. For larger projects with multiple audiences it may be
  worthwhile to set up a second mailing list for non-technical
  discussions or release announcements.
  
* **Testing saves lives.** Using automated testing helps you to check 
  that nothing has broken before you release code. It also helps 
  your contributors feel confident they have not broken code they are
  less familiar with.


## Hosting civic applications

* **Provide a demo system.** If you're providing a read/write API, it 
  can be useful for developers to have a testing instance that does not
  modify live data.

* **Supply testing data and database migrations.** To get people started
  with your application, it's very useful to provide some realisitc test
  data, perhaps even a part of the data used in the live service.
  
  Database migrations are small programs that help you transform the
  structure the application's data model changes over time. This makes
  it easy for other users to follow along when you make these types of
  changes.

* **Monitoring and logging.** You shouldn't rely on kind strangers to
  notify you when your app is down. Monitoring can be done using tools like [Nagios](http://www.nagios.org/). 

* **Learn about 12 Factors.** [The website](http://12factor.net/) lists
  factors that are significant for those offering web services to the 
  general public.

### References

* [Producing Open Source Software](http://producingoss.com/en/index.html)
* Noah Veltman's [principles on design](https://github.com/veltman/principles)

### Credits

This document contains contributions from [Friedrich Lindenberg](http://pudo.org), [Robert Gieseke](https://github.com/rgieseke), [David Lemayian](http://www.davidlemayian.com/), [Nick Stenning](https://whiteink.com/).
