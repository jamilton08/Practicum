---
description: How fast can I build my own calculator?
---

# Build A Calculator


## Introduction

Through our computer science course we have discussed how much more efficient a machine is at processing things faster than us humans so today we are to put this to the test. One might think that this is a simple task however, the most difficult part comes with the translation of human logic to machine logic. We will explore this today but luckily we will have pre structured templates and resources to guide us along the way

## Task

We will take a template that looks like the screenshot below





<figure><img src="https://github.com/jamilton08/Practicum/blob/main/src/initial_calc.png" alt=""><figcaption><p><b>Fig 1</b> initial template that you will recieve.</p></figcaption></figure>

and make it look like the one below with it being able to completely function, so 5 * 3 should equal 15 and so on.
<figure><img src="https://github.com/jamilton08/Practicum/blob/main/src/completed_calc.png" alt=""><figcaption><p><b>Fig 2</b> Completed Task</p></figcaption></figure>

You will be given a small walkthrough and its up to you to fill the details. Those details will be matched with some test cases provided in a seperate folder. This will go over everything in the following order.

* **Setup** 
 Where to find our folders in which we will begin working from

* **Walkthrough** : We will go through each file in the folder and see how we have to inject some code, resources will be provided along the way so please read careful
* **Submit** : We will guide you to a special folder which was written by HSCT. It's a webapp where you will submit your work and it will tell you your score. You can submit as many times as you like. So lets begin


Okay so now lets move on to setup

## Setup


We will navigate to our  `desktop` folder and we will look for a folder called `practicum`

<figure><img src="https://github.com/jamilton08/Practicum/blob/main/src/folder.png"><figcaption><p><b>Fig 3</b> Folder in desktop</p></figcaption></figure>

Inside you will find three files which are **index.html**, **style.css** and **script.js**. These files will be the ones you'll be working on. You might ask where will we be working on these files from and that's a ledgit question. We will be working on these files from `VS Code` which you can find by putting "vs code" on your search bar on the bottom of your `Desktop` and the icon should show up. Now double click or execute it to your liking. 

<figure><img src="https://github.com/nycdoe-cs4all/interactive-web/blob/main/.gitbook/assets/Screen%20Shot%202023-03-01%20at%2012.07.51%20PM.png?raw=true" alt=""><figcaption><b>Fig 4</b> <p>Hover over <i>file</i> then <i>click open</i> and it from there you can navigate to <b>Desktop</b> then open <b> Practicum </b></p></figcaption></figure>

### Important Observations

* We've worked with **VS Code** before when we used codespaces so everything works similar. Top left icon is where your files will be and it will be the only tab you will need for this project.

* you can save by hovering <i>file</i> on top then click <i> save or save all </i>

* you can preview and test your current work by navigating to `Practicum` from your `Desktop`, right-click **index.html** and opening with any browsers that show up.

## Walkthrough

Okay so now in that we are in **VS Code**, lets head to index.html.
Lets look at **line 12** and we see a line as such 

```html
<input type="text" readonly>
```

Let's add an id "display" inside this element. We've covered this before so if need help feel free to ask your tech teacher for a guide. Now we can head to **line 14**

```html
<div>
```

we would like to add a class called "keys" to this element. Ok now lets look at **Fig 2** and we notice the configuartion.

```html

<button onclick="appendToDisplay('7')">7</button>
            <button onclick="appendToDisplay('8')">8</button>
            <button onclick="appendToDisplay('9')">9</button>
            <button id="clearDisp">C</button>
            <button onclick="appendToDisplay('+')">+</button>
            <button id="equal">=</button>
```

The configuration of buttons above doesnt seem like their in the same order so lets append the missing buttons just like shown above to have all buttons listed on **Fig 2** and then lets move on to CSS.

Our Buttons will sort of look like that in **Fig 1** and we want to structure it like that in **Fig 2** so we will use a property called `grid-template-columns`, look below to see resources and where we will enter it which should be in your <i> style.css </i> file between lines 30 - 33. Play around and see how it works

```css

.calculator .keys {
    display: grid;
    /*
    documentation1 in ----> 
    https://www.w3schools.com/cssref/tryit.php?filename=trycss_grid-template-columns 

    documentation2 in ---->
    https://www.w3schools.com/cssref/playdemo.php?filename=playcss_grid-template-columns
    */
    gap: 10px;
}
```

After this your app should look just like **Fig 2**

Now let's move on to **Javascript**,
so in our html file we made an element to have the id of display, now lets make a `const` and get the id of "display" and assign it to that constant and lets name it **display**

```javascript
const display = document.getElementById('display');
```

When we click the button with id "clearDisp", we would like the function `clearDisplay()` to be called

when we click the button with id "equal", we want `calculate()` to be called

for `appendToDisplay(value)` we would like to add the value to our display. 
You can use `display.value` to access the value property that's inside your display and even change it.

for `clearDisplay()` we would like to clear our display completely also using `display.value`

## Submission



