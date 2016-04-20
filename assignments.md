---
layout: page
title: Assignments
---

### List of assignments

{% for assign in site.assignments %}
- {% include link.html target=assign %}
{% endfor %}

### FAQs

**What is the expected assignment workload?**

There are 9 assignments over the quarter, one per week. 
We expect the assignments never to take more than an hour and frequently much less.

**What programming environment and tools are used?**

Students will use their own computer for the assignments.
If you use a Mac,
you will be using the Terminal program and unix command line tools.
If you own a Windows laptop,
you will install a virtual machine running Ubuntu linux 
and you will use the virtual machine for your assignments.

**What is the assignment collaboration policy?**

The programming assignments are to be done individually and should represent
independent, original work. We adhere to the Stanford and CS department Honor
Code policies, and offer specific examples of its application to CS107E
coursework in our [course collaboration
policy](/policies/#collaboration-policy).

**How do I submit an assignment?**

Assignments will be submitted online using `git`. 
Don't worry, we'll walk you through the process.

**How are assignments graded?**

You'll get credit for any good faith effort on the assignment.
