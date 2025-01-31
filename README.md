# Events and Debugging Assessment

Time to assess how well you have learned to use the debugging tools in Chrome Dev Tools, and writing click event listeners. This application is to show kids with illnesses and the memories the would like to make. Celebrities sign up to help kids make memories.

> 🧨 Make sure you answer the vocabulary and understanding questions at the end of this document before notifying your coaches that you are done with the project

## Event Listeners to Create

1. When the kid name is clicked, it should display their wish.
1. When the celebrity name is clicked, it should display their sport.
1. The pairings list should should contain the pairing in the following format.
    ```html
    {child name} will be making memories with {celebrity name}, a {celebrity sport} star, by {child wish}
    ```

Below is an animation showing how the application should look when complete and how the event listeners should work.

<img src="./images/debugging-events-assessment.gif" width="700px">

## Setup

Your instruction team will provide a link for you to create your assessment repository. Once your repo is created, clone it to your machine.

1. Make sure you are in your `workspace` directory.
1. `git clone {github repo SSH string}`.
1. `cd` into the directory it creates.
1. `code .` to open the project code.
1. Use the `serve` command to start the web server.
1. Open the URL provided in Chrome.

Make sure your Developer Tools are open at all times while working on this project. Use the messages provided in the Console to determine what code needs to be fixed or implemented, and use breakpoints in the Sources tab to step through your code as you debug.

## Vocabulary and Understanding

Before you click the "Complete Assessment" button on the Learning Platform, add your answers below each question and make a commit.

1. When a child is clicked on in the browser, which module contains the code that will execute on that event happening? Can you explain the algorithm of that logic?
   > The code for that click event is contained in the Kids.js module. The code is using the document.addEventListener method to look for anytime someone clicks somewhere on the page. It then takes the target of that click event and checks to see if it matches the data type "child". If it is a match it then references the appropriate data sets from the HTML generated in that module and then performs a window alert containing the child's name and their wish.

2. In the **Pairings** module, why must the `findCelebrityMatch()` function be invoked inside the `for..of` loop that iterates the kids array?
   > The `findCelebrityMatch()` function is invoked inside of that for..of loop so that each iteration of the kids array can be passed as an argument to the function. This way we are invoking the function multiple times until we have iterated through the entire kids array. 

3. In the **CelebrityList** module, can you describe how the name of the sport that the celebrity plays can be displayed in the window alert text?
   > This is accomplished by referencing the data attribute sport that is set in the HTML generation in this module. To do this I took the target of the click event and set it to the variable 'itemClicked' then I defined a new variable 'celebSport' to 'itemClicked.dataset.sport', this stores the 'sport' data attribute for whatever was clicked on in the 'celebSport' variable. I then use that variable in my window alert. 

4. Can you describe, in detail, the algorithm that is in the `main` module?
   > The main module starts by importing the functions responsible for generating our HTML 'Pairings, Celebrities, Kids' so that we may invoke them when generating our application HTML. It then uses the document.querySelector method to target the container element and sets it to the variable 'mainContainer'. It then generates the HTML for the various sections of the page and invokes the imported functions for their corresponding section. That HTML is set to the variable 'applicationHTML'. Then we take that stored HTML and place it inside of the mainContainer element.
