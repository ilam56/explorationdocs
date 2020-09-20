# Starting explorations
I started out by reading the links in the basic reading section of my source/Source.md. I also did a bit of additional skimming of information on the angular docs page.

## Creating sample app
I followed the tutorial at https://angular.io/start to create a simple sample app to familiarize myself with angular. I then messed around with the app and tried changing various things
I explored a bit about how the various components and views connected to eachother. This exploration led me into trying to figure out about routing.

## Failure to upload
I ran into huge issues trying to upload the code to apache server. I spend about 2 hours with the T.A, but ultimately had to give in and just host it on stackblitz.

## Basic routing.
This is where I started to learn a bit more about the code. I used https://angular.io/guide/router as a guide to explore how routing worked and got a basic understanding of it.

# Creating an App.
I decided  to create an app that would show off both routing and some new skills I would soon pickup. My original plan was for the main page to have route switching between a few apps I would create and the sample page, but for reasons I will point out later, that did not work out. That said I started off my getting the routing looking nice before starting to code a working app

## The Calculator.
For my App I decided to create a simple calculator with basic addition, subtraction, multiplication, and division functions. It started off fairly well. I first got the page all set up with all the buttons and did the css to make it look at least a little presentable. That is when I realized I could load the buttons in a similar way to the sample project by loading them from a buttons array object.

## The buttons
The issue I had with the buttons is that I needed to sort the object array by column. Unfortunately I had trouble finding a good way to do that and the few ways I did find ended up not working. I spent a good 45 mins trying to get those darn buttons to work, but in the end I had to do a workaround of sorts. I found that I could sidestep the problem by just ensuring the buttons were in the proper order inside the buttons.ts file. This was a very simple solution, but one I would prefer to correct as it damages scaleability. All said in done, I did still have buttons beging loaded by a combination of a ngFor directive and a ngIf directive. That in itself was a bit of an issue as I found I had to add an additional container just to use both together. Thus, my resulting html takes in buttons with a label and row and puts then into a ul with a li for each row. It then creates buttons filled with their label that send their label to an update function when clicked.

## The implementation
Next was the implementation. Was fairly straight forward. That said I did need a bit of help with some of the syntax for the methods and functions. The main challenge was creating an update method that would work for all the buttons. It was fairly simple for most of it. I simply checked if the incoming label was a number or not and if it was I updated the current value with the number, and if not I used a switch to chose the correct action. I ran into a bit of trouble with problems for edge cases when user presses strange buttons. For example, pressing the + key multiple times without inputing anything. In the end it was just some simple logic and error checking though. The main thing I learned from the implementation is how to better use typescript and it's functions. The biggest issue I had was a problem with chain arimitic. I wanted it so that the user could enter in, for example, 99 then press '+' then press '1' then press '-' and '5' and it would output the correct answer for 99+1-5. However, for some reason this caused all sorts of problems with the way I did things, thus I decided to simplify the problem massively by requireing an equals press between each operation.

# The big problems
I ran into an enourmous amount of small problems, but not actually that many larger ones. Mainly things with logic not working and strugling with the angular directives.

## The crash
So at one point when I was working on my stackblitz page, the page refreshed. Now, I am pretty sure I had clicked the save button multiple times, but I think that for the changes to stick I needed to hit the commit button. Needless to say, I lost about 3 hours of work. Fortunately the work went faster the second time and I only took about half that time to get back to where I was. Unfortunately, It was because of this crash and a few other problems that cropped up that I wasn't able to do as much as I wanted. That said, I personally thing I did well enough even without the extra stuff I had planned.

## Unfamiliar with typescript/javascript
So I do have a little familiarity with some of javascript, but ultimately I have not worked on it as much as some other languages and so I ran into quite a few barries where I had to look stuff up only to be frustrated that the solution seemed so overly complex that it ended up better off to just find a work around. I am still quite sure many of my problems had easy solutions I just couldn't find.

# What did I learn?
I learned quite a bit in this exploration. There was a lot of tinkering and reading. Many of the links I read I didn't bother putting under sources, mainly because the information in them didn't actually contribute to my application in any way. That said I still read them and learned, so I guess you could say they were helpful.

## Basic directives.
I learned basic use of directives. The main way I did this was by using them for the buttons as I mentioned earlier. In particular I learned about ngFor and ngIf, but I also read about other directives.

## Routing
I learned how routing works and how it decided which page to display in the route outlet. I did this with a combination of playing around with the sample app and following the tutorial I mentioned above.

## Basic syntax
I got a refresher on typescript and javascript and learned a bit about the syntax needed from angular. For example, how variable and methods are declared as well as how to create classes and modules.

