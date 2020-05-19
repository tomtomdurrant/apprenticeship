# Bootcamp 7 - Testing Pyramid

What is a tester? There are many different types of tester, with different names.

ISO9001 is a standard to ensure quality

Automated tests allow testers to focus more on the high value exploratory testing rather than the basic stuff. Automated testing goes hand in hand with agile development. 

#### What testing do I need to do? 

There are many different styles of testing with different tools 

#### What is manual testing

Discover stuff that might be broke.

Check interactions that you haven't thought about before.

**Important to write manual test cases so the steps are repeatable**

Acceptance tests will tell you what the application should do - not how good it will be. Other things that could also go wrong.

Visual regression tests? - Is the website working? 

Developers should own the tests. 

What is the main priority of the application - e.g. IPlayer - does it play the video? 

Headless browser - is it broken? 

### Unit testing

Small tests which give us confidence in our code.

Tests should show intended behaviour and test names should be descriptive.

In TDD - do the tests fail in the way you expect them to? 

#### What makes a good test?

Keep the test simple

Don't intertwine your tests.

https://www.maxpou.fr/10-tips-write-better-tests

#### Contract testing

Ensures that a pair of applications will work correctly together by checking each service in isolation to ensure the messages it sends or receives conforms to that contract. 

### UI Testing

Fragile, slow and expensive to maintain.

Slow and hard to run in automated CI.

## The V Model

Not agile

![image-20200518113745605](C:\Users\uktdur\AppData\Roaming\Typora\typora-user-images\image-20200518113745605.png)

#### Usability testing

Testing the user experience and it's ease of access/ease of use of a product. 

Compatibility tests - browser stacks

#### BDD

Behaviour driven development

Given when then.

## Testing - The bigger picture

Everyone should test.



# Day 2

**Fakes**: real implementation with some functionality - an in memory database

**Stubs**: something that returns a pre-canned response

**Mocks**: something that records the calls on it

#### Fakes

Can make tests slow and unreliable as you are depending on code that is not used in production.

#### Stubs

Can be easy to add without additional tooling. Just enough data to make sure that everything works. 

#### Mocks

Allows you to check calls made and is very powerful. Can also do the job of stubs (used interchangeably).

---

**Only mock what you own**

You tie tests to implementation that might change and you do not control.

This gives you a false sense of confidence that your tests and everything is ok but it isn't.

e.g. mocking a Date function - the implementation might change at some point in the future. 

#### What you should do

Create a seam/wrapper object that you can control so you can mock it.

`function today() {return new Date()}`

Now: Better code, clearer and less couples

Easy to mock as I only need to mock my function. 

---

### Visual Testing & testing the front end

Some tests are very helpful but too many can be inefficient 

**Selenium IDE** - ability to automate selenium.



## Links

What makes a good test?
https://www.maxpou.fr/10-tips-write-better-tests

Contract testing
https://docs.pact.io/
https://sendgrid.com/blog/quickly-prototype-apis-apiary/
https://help.apiary.io/tools/mock-server/

Usability Testing
https://uxdesign.cc/10-usability-heuristics-every-designer-should-know-129b9779ac53
https://www.interaction-design.org/literature/topics/usability

Acceptance Testing
https://danashby.co.uk/2016/08/23/acceptance-testing-what-does-it-mean/
https://www.developsense.com/blog/2010/08/acceptance-tests-lets-change-the-title-too/
https://youtu.be/SBhgteA2szg 

BDD - Cucumber
[docs.cucumber.io](http://docs.cucumber.io/)

Exploratory Testing
https://www.satisfice.com/exploratory-testing

Test doubles, fakes, mocks and stubs

https://blog.pragmatists.com/test-doubles-fakes-mocks-and-stubs-1a7491dfa3da?gi=e45b923fe226

https://kata-log.rocks/starter

https://github.com/emilybache/GildedRose-Refactoring-Kata/tree/master/python

https://understandlegacycode.com/blog/3-steps-to-add-tests-on-existing-code-when-you-have-short-deadlines/

https://www.youtube.com/watch?v=8bZh5LMaSmE

https://martinfowler.com/articles/mocksArentStubs.html

https://github.com/sandromancuso/trip-service-kata

https://blog.pragmatists.com/test-doubles-fakes-mocks-and-stubs-1a7491dfa3da?gi=e45b923fe226