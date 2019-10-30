# Hands-on QA Assessment

----

## Introduction

This is a hands-on test scripting challenge where you'll be asked to write end-to-end tests around some acceptance criteria.

For this challenge, you can use any test framework you like. We recommend using [Cypress](https://www.cypress.io/), [Puppeteer](https://github.com/GoogleChrome/puppeteer), or [Selenium](https://www.seleniumhq.org/).

We're not using any endpoints here, so we don't need to worry about mocking any server data or doing integration tests against an API. We'll be focusing on writing feature tests that drive through the user scenarios documented in the mock acceptance criteria below.

### Important Note

The kind of tests we're looking for here are end-to-end, not unit tests. Therefore, we don't want you to test smaller parts of the application. We'd like you to test the application by running it through user scenarios in a headless browser, where you're simulating user input and walking through full user scenarios.

----

## Acceptance Criteria

For the purposes of this challenge, we'll be using the TodoMVC application, which is a basic ToDo app. All of the code for this application has already been written. You'll check out the project code, and write tests that check for each of the following acceptance criteria:

* When loading the page, you should see a navigation bar with the following two options:
  - Search Etsy Catalog (selected)
  - About the Developer
* When clicking on "About the Developer" in the navigation bar, you should arrive at `/about` and see:
  - An h2 tag with the developer's name
  - 5 portfolio links
* When clicking on "About the Developer" and subsequently clicking "Search Etsy Catalog", you should return to the original view
* On the "Search Etsy Catalog" view, there should be an input box to enter a search term with the placeholder text "Enter a search term here"
* On the "Search Etsy Catalog" view, there should be a search button with the text "Search"
* When initially loading the "Search Etsy Catalog" view, there should be a list of 25 links to product listings at Etsy.com
* When entering a search term on the "Search Etsy Catalog" view and pressing the Search button, the following should occur:
  - An XHR should be sent to:  `https://openapi.etsy.com/v2/listings/active.js?page=1&keywords=<keyword>&api_key=<apiKey>&callback=etsyJsonp2`
  - 25 different links should appear in the list below the search form

----

## Assignment Steps

### Step 1: Check out the test project

Clone the git repository at:
https://github.com/crates/react-etsy-client

### Step 2: Run the project locally

Run the project locally by typing:
```
npm install && npm run build
```

Now, your server should be running locally automatically. Open up a browser and head to http://localhost:4000/ to confirm.

You can now start writing tests. If you have any issues running the local server, try testing against [the demo site](https://etsy-react-client.surge.sh/) instead.

### Step 3: Write the tests.

Please write tests around each acceptance criteria, ensuring that they pass.

### Step 4: Send us your results.

Take your test code, and the output of running your tests, compress them in a .zip file, and send both files back to us.

----

Good luck! Thanks for taking the time to complete this assessment. 

Please also double-check with your assignment contact to see how long you have to complete this task.
