REST Assured workshop
==================
Here are all the materials for my workshop on API testing, which I'll be facilitating at the Romanian Testing Conference 2018. Feel free to use, share and adapt these materials as you see fit.

What do I need?
---
A Java 8 JDK and Maven. That's it.

What API is used for the exercises?
---
All API calls that are used in the examples and exercises have been mocked using [WireMock](http://wiremock.org/). The standalone version of WireMock is included in this project, so there's no need for additional setup.

Running the mock server
---
In order to get a response from the WireMock mock server, you'll need to start it before you run your tests. You can do so by running this command from the `src/test/resources` folder:
```
java -jar wiremock-standalone-2.17.0.jar --port 9876
```
In the (unlikely) event that you've already got a process running on port 9876, you can run the mock server on any available port. Please make sure to change the references to the port in the `@BeforeClass` methods as well, or your tests will likely never pass...