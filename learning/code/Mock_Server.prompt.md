\###Role: 

You are an software architect who has well knowledge and understanding of System architecture, software design knowledge and well expert in technology stack. You also have well knowledge and understanding of how applications in Windows and Mac.

Work: I need you know to understand the technology stack of Windows and Mac and build a Mock Server tool that is production ready with different modules that can be scalable, reusable and follows software design pattern. Take Fiddle as an example.


\###What is the issue:
Right now we use Chrome DevTools to mock the API responses. The problem with Chrome DevTools are

* It cannot properly mock response headers.
* It cannot mock response status code, cookie.
* It cannot mock API with same path, that is if both API has similar paths like "/v1/accounts/{accountId}" and "/v1/accounts/{accountId}/offers" then I can't mock both at the same time.
* It does not allow wildcards to use for API paths to identify and mock.
* If I need to mock same API for different users and if each user has different user-id, then each time I need to mock.
* If I mock one API in Tab-1 and in new tab if I need to mock the same API then I need to open the DevTools and use the same API in order to have same user-id in the URL.

\###Feature of the Mock Server:

* Mock Server should be able to identify the API or network calls made from the applications such as Windows apps, Chrome Browser, Edge browser, Postman etc and send the configured mock response to those applications.
* Mock response should be able to configured through json file, XML file, text file or JavaScript code, that code follows certain logics to send the mock response to the application which initiates the network calls.
* I should be able to mock the response header, cookie, status code and body.
* It is not mandatory to mock the response header, cookie, status and body all the time. Sometimes I may need to mock any one of those.
* I wanted an additional feature where when needed the mock server (this tool) can call the actual server and get the response and based on the mock configurations configured in the mock server, only the specified parts of the response get mocked and rest of the data returned from the original server is used to send to the application.
* I should be able to mock the API which has same path.
For example:
If I wanted to mock "/v1/accounts/{accountId}" and "/v1/accounts/{accountId}/offers" and "/v1/accounts/{accountId}/offers/discount" I should be able to mock them without any issues and send custom responses individual for each endpoint.
* I want the mock server to have proper logs configured so that it helps me to identify what network calls are intercepted, what mock rules is set, what mock data is used and what is sent back.
* Logs should also help me to debug if there are issues and helps to identify what happened at each stage.
* This mock tool should identify how applications works in Windows and Mac and should able to identify the network calls happening in these platforms and work accordingly. It should be Windows and Mac compactible and works well.
* I need to use wildcards or pattern matching for identifying the API URLs. Example, if the API URL has "/v1/accounts/{accountId}/offers" then I need to use wildcard or pattern matching like "/v1/accounts/\*/offers". So that it matches for all user-id.
* I should be able to more than 1 mock data file available for every individual API response. I will be using any 1 mock data for individual API but I should have ability to maintain variant-A response, variant-B response, Response-1, Response-2 for individual API. So that if needed, I can switch to different variants, I no need to recreate it every time.


Identify any other betters available in Fiddler mocking tool and build those features.

\###Note: The first priority is given to "Windows Operating System" and build accordingly. All the features should work fine with "Windows".


\###Implementation:

* First read and understand the requirement, what is the present issue with the Chrome DevTools.
* Understand the user requirements.
* Identify how the Windows Operating System works, how the network calls are made and how it architecture and implemented.
* Identify how the Mac Operating System works, how the network calls are made and how it is architecture and implemented.
* Identify how the networking concepts are working with Windows applications, how to identify the network calls made from Windows and Mac operating systems.
* Read and understand all those details. Refine it, iterate these steps until you get a very clear vision to proceed further.
* If you miss any information and if you feel any other information is needed, search the web and get all the required information's analyze and understand those keep.
* Keep everything in memory.
* Create or draft a proper plan, iterate the planning process until you find better best fitting plan and create it in a file to read, check and verify. Plan should include what programming languages and supporting packages or libraries to use.
* Start working on the implementation to create the Mock Server tool.
* Build the necessary modules, networking concepts and all other codes required.
* Once you have build the app.
* Make a proper full end to end regression test to check if the tool works.
* Check if all the features are implemented and working.
* If any issues found, identify the root cause of the issue, and fix those bugs.
* Once the bugs are fixed, retest it again.
* Once all the bugs are fixed run a final end to end regression test.
* Until all the issues are fixed, rerun the test again and again.

\###Rules:

* Build the Mock Server Mainly STRICTLY compactible for "Windows Operating System"
* Follow Software coding principles, design principles and other related software development principles.
* Create the application as memory optimized and speed optimized. That is create it with better space and time complexity.
* STRICTLY DO NOT ASSUME ANYTHING.
* IF YOU HAVE ANY QUERIES ASK IT GET IT CLARIFIED AND START PROCEEDING.
* Make a proper research and understand and learn from it and then start writing the code.

REPEATING: DO NOT ASSUME ANYTHING. If you have any doubts ask it get it clarified and then proceed.

