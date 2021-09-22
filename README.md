# Timeless backend coding challenge

Hello and thank you for taking the time to try this out.

The goal of this test is to assert (to some degree) your coding and architectural skills. You're given a simple problem so you can focus on showcasing your development techniques.

As this is a code review process, please avoid adding generated code to the project. This makes our jobs as reviewers more difficult, as we can't review code you didn't write.

_Note: While we love open source here at Timeless, please do not create a public repo with your test in! This challenge is only shared with people we're interviewing and for obvious reasons we'd like it to remain this way._

## The tasks 🏁

### Problem Solving

Write a program that prints the numbers from 1 to 100. But for multiples of 3 print "Hey" instead of the number and for the multiples of 5 print "Ya". For numbers which are multiples of both 3 and 5 print "HeyYa".

### Node.js (with Typescript), Micro Services and Databases

Assume a platform where collectibles are sold in form of fractions. An asset ( **asset** - see sheet under /tables) is split into shares (like stocks of a company). Each asset is a one of a kind item and can not be restocked. The **total_amount** is the total available quantity of shares of this asset. Users then can buy shares on the platform. The system is a **microservice** architecture where the AssetService maintains the list of all available assets and their corresponding quantities. The AssetService is the source of truth when a user opens the app and sees the stocked asset and the available shares for each of them.

#### The Task

Write a small OrderService which allows users to buy shares of the assets from the AssetService. Please be aware that this is a high peak load scenario, where users can not buy at all times, but are limited to drop days which are set to certain days and have a specific start and end time. Possibly hundreds and thousands of people might try to access the system at the same time and want to make a purchase.
- Make sure, that every user has the time to pay for his reserved shares!
- Make sure, that you do not sell more shares than are available in total!
- To keep track of the orders you should create an order book
- The microservice should offer endpoints to create an order and to get a list of orders for a specific user.
- The microservice should also handle payments (no real payment provider integration needed, mokup is fine)
- The orderService shall access the AssetService via HTTP(s) (not limited to REST, chose what ever you think suites the case)
- For time constraints: You don't have to implement the AssetService. Just work with assumptions. What we want to see is the approach of solving the problem. But of course some real SQL queries and working code in the OrderService context is required.
- writing tests is also welcome

_Notes: Feel free to introduce more order and asset statuses and change the status accordingly._


## What will we be looking at

- Attention to detail and scalability
- Code reusability, readability and maintainability
- API security, data validation etc.
- Finding the right point of abstraction in your helpers functions and APIs

## Evaluation Criteria

- You're free to use as many third party JS libraries that you see fit
- Tests, type checking, linting... are nice to have

##### Happy hacking!
