# UFO
Groupe: Team UFO
Gordon Mikkelsen
Hassan Mohdi
Yakubu Adeyemi Oseni
Kristoffer Rath Hansen
UFO Blog Entry
                              ## Deadline! Thu. Nov. 28th 8:30 am
Abstract
This report examines the difficulty of writing proper integration tests. In the report, we will go through sub-questions based on our main problem where we will among other explain some examples of how integration is done and state our thoughts.
We will then later explain some theories on integration test in order to have a better understanding of how those kinds of tests are done.
This is interesting because even though proper integration tests are hard to write they are still popular to use. 
What is also interesting is if they are so popular, then why have anyone not  come up with an easier solution as to writing proper Integration tests?    
Our solution achieve us having an understanding on why it's hard to implement integration tests.So what follows then is that by having a clear understanding we might  be able to come up with a solution ourselves on writing proper Integration test.
The report finishes off with explaining our solution for those integration tests we made and how they were made


### Introduction
We have in Large system been giving the assignment on creating a system for a Hotel chain in which we have to create a system where a backend part talks to our frontend part via a contract where both systems are written in the same language.
Where for the backend we have created the project as a wcf project not necessarily any reason  as to why other than it is properly easiest have it written in C# So for the front part we created it in ASP.NET because firstly as mentioned before the demand from the assignment was that both frontend and backend had to be written in the same language and secondly it is the newest technology from the .NET world which is a lot easier having it integrated and talking to  our backing system. 
By having these two systems talking to each other we use a contract.
The contract is an Interface where we created a nuget package from out of it, which is then used in the frontend-part. 
To make sure we always have a product ready we use a build-server and then have continues deployed up on Azure were the data is stored on mysql server. To make sure the requirements  are proper implemented we have in our project we have implemented test cases, so we can get an overview over if we covered the things we wanted. So far we only use unit tests in the backend. 
Our thought was to research if it would be helpful for us to make some integration tests - even though they are hard to write properly. This leads to our following hypothesis
Hypothesis
Integration tests are hard to write properly, but just a few good ones are really helpful.
Analysis
What is an integration test?
an integration test is the second level of software testing which is usually made after unit testing where the different compounded are combined as a group and therefore tested. which make it easier to find faults in the interfaces and in the interaction between integrated units. Test drivers and test subs can also be used to assist integration testing to make a more clear and a better integration test. 

There are  different approaches as to how on conducting integration tests
For example, one way could be a top-down in which we start testing from the GUI and then work all the way down to the database or vise versa (Ref)

Another way of doing an integration test could also be if you have an interface that is exposed then you can that tests since it is integrated into the different parts of the system.

This is not so much an integration test in it self , but to reduce integration problems it is quite common to set up continuous integration for the project e.g having a build server.  The build server then makes sure every time there is a change in the code it automatic builds, making a lot easier to discover bugs in our system

Collection of unit tests - not to replace unit tests, but to test the integration between them
Explain our idea on how we will create an integration test for our Hotel system
Firstly we want to do an integration test so we are making sure that we test all of our system.But also because our system do not contain that not many lines of codes we thought that it might be easy to do integration testing.
On how we will do the integration we think maybe try a top-down approach where we go from testing the GUI all the way down to the database. Another idea was creating some mockups and having to test our Interface. 
We will also want to set up a build server so we can reduce integration problems
Explain how we have tried to implement our integration test
We implemented an integration test to make sure our search form for Hotels is shown correctly. This way we don’t have to write unit tests for everything, but we can simply test that the output contains the correct elements.

While searching for hotel availability on the HotelChain, the search need to use various modules to give us  expectatious value from the search from a particular cityY 
Explain our thoughts on where we have succeeded and failed on doing integration test 
As to where we have succeeded, we believe that because we have created an integration test conHtra nothing at all, that in itself is a partial victory.  On the other hand, we sort of failed in doing the test or more pr in regards to doing a proper integration test which leads to not having covered most of the bugs in our system. 
Why are integration tests helpful?
It helps realize if the build fails for some reason before committing it all. Integration test do also tell you whether it is working compared to unit tests which only tell what is not working, so as long as everything is working you actually don't need unit testing but it still nice to have them if something is wrong. Integration tests make you able to check a whole use cases of your application. Where unit tests only check low-level logic in your application. So to keep track of the state of your project, Integration testing is very useful since you know if your use cases are working, which are also especially useful for a manager of a project to feel safe about the project
Why are they hard to write properly?
It’s hard to catch exactly what scenarios will probably fail so we get 100 % code coverage.
They are also hard to do proper because when doing integration test , you have to test all of what the system contains , which means all the code,  live  versions of services and interactions between all the modules. This is of course is on the premise that one has access to the network otherwise the integration test would be for granted.
 
What makes a good integration test helpful?
It helps us to check all the logic implemented by the modules or components to test if they produce the expectations and rendering the correct value, such as when we finish developing various components in our system, we needed to test if the booking of the hotel could be done successfully.
In addition, Drivers can be used to call the functions of the lowest module in case the calling function does not exist. Stubs that can accept the inputs/requests from the top module and returns the results/ response could also be used to perform make a good integration test helpful.

If they are helpful then why only a few of them?
When we write an integration test, we want to make them good, but since they are hard to write, our time is best spent writing a few good ones.
A few good ones will still help us massively since it is likely that we’ll catch something if something goes wrong. This is due to the fact that integration tests cover a lot of code, simply by looking at what we get back instead of looking at a single piece of code.
	
Conclusion
In this blog entry, we have covered our hypothesis, “Integration tests are hard to write properly, but a few good ones are really helpful” and explained how integration tests help us, and why we think they are hard to write properly.
We have gone over our implementation of integration tests and reflected on good and bad things regarding this.


References
https://stackoverflow.com/questions/1788436/why-using-integration-tests-instead-of-unit-tests-is-a-bad-idea (27/11)

https://martinfowler.com/bliki/IntegrationTest.html(22/11)

http://softwaretestingfundamentals.com/integration-testing/ (25/11)
https://en.wikipedia.org/wiki/Integration_testing (24/11)

