# feed-reader-testing

Feed reader testing is using Jasmine framewor.

# Table of Contents

* [Project Overview](#project-overview)
* [Run the Application](#run-the-application)
* [Test Instructions](#test-instructions)
* [Contribution](#contribution)
* [Acknowledgment](#acknowledgment)



# Project Overview
In this project a web-based feed reader application is given. [Jasmine](http://jasmine.github.io/) framework is used to test the application. 

# Run the Application
In order to run the application user can:

* Clone the git repository 

  `https://github.com/coolrab/feed-reader-testing.git` or

* Download the .Zip file to the local machine.

Access the folder and open index.html to load the application in a browser.

# Test Instructions

Here are the test suites written in Jasmine.js

## Test Suit "The Menu"

First test case of this suit ensures that the toggle-able menu is in an initial state of `“hidden”`. By inspecting the menu toggle events in Chrome dev tools, I have observed the program show and hide the slide menu bar by toggling class `'menu-hidden'` on <body>. So I have written a test which checks for this hidden class on the body:
  
 Second test check whether or not the menu toggles on and off. For this test however, we need the `menu icon element`. We can find this element through dev tools.Once the 'menu icon element' is identified we need to query and store this menu icon element in a variable. Next, we want to “click” this element by using `click()` method.

## Test Suit "Initial Entries"

In app.js, it runs `loadFeed()` to load the data from each feed. If the feed load successfully, it renders the HTML inside the feed container `DIV.feed`.

Since class `.entry` is a rendered element when feed successfully initialised, by checking the `.feed HTML` after loading can be seen if the entries has been loaded properly.

The `loadFeed()` is asynchronous so that the test should run `beforeEach()` and `done()` methods to ensure the `loadFeed()` runs in the test.

By calling `loadFeed(0, function(...))` test load the first feed which contains initial entries for detection.

## Test Suit "New Feed Selection"

There are more than one feed in the allFeeds. The loadFeed() function load specific feed with the id(index).

The second feed content should be different from the first feed. So by comparing the rendered HTML content, it is possible to check if the program loads a different feed with the function instead the same one. Following tst case is written to check the feed is changing accurately.


# Contribution

You are **welcome** to contribute to this project.

Here are some ways you can contribute:

- by reporting bugs
- by suggesting new features
- by writing or editing documentation
- by writing specifications
- by writing code ( fix or add js files, add comments, modifying styles)


#### THANK YOU ...

