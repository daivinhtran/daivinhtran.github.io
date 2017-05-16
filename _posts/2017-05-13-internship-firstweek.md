---
layout: post
title: Internship - First Week
tags:
- Internship
- Week1
- Software Engineering
- SF
---
## Day1&2:
The first two days were mainly orientation and meeting with the teams.

## Day3:
I was able to move a ticket from “To Do” -> “In-Progress” -> “In Review” and finally to “Done”! Everyone in the team was so excited. My manager thanked me “for getting up and running quickly!”

## Day4:
Then came to the 2nd ticket in my day, it was simple too. Wrote some code, push it, and made a pull request. Got code review feedback on my code in about 20 mins. “This is great. But just a few notes…” My team’s feedbacks are all great. I went back to refractor my code and added a few unit tests which all passed “locally”. Push it. My coach jumped in and gave me another code review. “Great! But since this is an integration test instead of unit test, are these lines of code necessary?”.
I “googled” “What is the difference between integration test and unit test?” and found [this](http://stackoverflow.com/questions/10752/what-is-the-difference-between-integration-and-unit-tests). Integration tests are used to reveal if a feature is working or broken. They invoke one or more software methods or features and test if they act as expected. Hmmm. My coach was right. The code I implemented for the ticket was for an user interaction. It should have been an integration test.

## Day5:
I spent my whole Day5 to change the tests from unit test to integration test. I found it’s extremely challenging to mock user interactions. I spent the day to debug my test instead of the actual implementation for the feature. And finally got it with the help of the EmberCommunity slack channel.
A little piece of knowledge in ember-qunit that I took me a whole day to finally realize:
In unit test, this.$() is scoped to the component
In integration test, this.$() is scoped to the test container. this.$('>:first-child') is scoped to the DOM for the component.
This is it! Two tickets in 3 days!

#### Things that I’ve learned this week:

* Basic in Ruby and EmberJS
* Difference between integration test and unit test
* How to learn in a big code base
* Attitude is important
* And finally …
* Every line of code that I write will be read by someone. Make sure it’s understandable