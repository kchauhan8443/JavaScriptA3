# Assignment 3

## Purpose

This vanilla JavaScript web app displays various daily menus which can be viewed by clicking either the next or previous buttons.  

![Image of app](app.JPG)

## Concepts Learned

To create this "Bun on the Run" menu app the following JavaScript concepts were used:
- variables let vs const
- _let currentIndex_______
- _const nextmenu____
- _______________
- _______________
- _______________
- _______________
- _______________
- _______________
- _______________

## How I made the web app

1. First I defined a const called menus and assigned it to be an empty array
    ```js
    const menus = []
    ```
    The reason why I did that is because the menus array will eventually be assigned an array of objects where each object represents a daily menu, complete with menu items and prices.

1. Next I ___defined const currentIndex and assigned it to be 0 ______
    ```js
    let currentIndex = 0;
    ```
    The reason why I did that is because _____To make the the array key editable
    

1. Next I defined ___const h2______
    ```js
    const h2 = document.querySelector("#menu h2");
    ```
    The reason why I did that is because ___my dom____ to edit the menu title that is my array in the html title 

1. Next I defined a _______ to display all today menu from my array
    ```js
    function display(todaysmenu) {
        menuTitle.textContent = todaysmenu.title;
        soup.title.textContent = todaysmenu.soup;
        soup.price.textContent = todaysmenu.soupPrice;
        ...etc...
    }
    ```
    This function displays the current menu.  For exammple, it displays the menu title by ________________________________

1. Next I defined a function called getJson which will fetch our menus data in JSON format
    ```js
    async function getMenu() {
        const res = await fetch("____________________________");
        const data = await res.json();
        menu.push(...data);
        display(menu[currentIndex]);
    }
    ```,
    First I defined a constant called res which will be assigned _ await fetch(url)___to load the json file
 
    Next I defined a const called data which is assigned __await fetch res.json()___to get the data from the loaded json file___.

    Next I inserted that entire array of objects into our menus array by _____pushing is with spread operator_____.  

    Next I called the function display to display our current menu passing in the argument of our first menu in our array

1.  Next I defined a function called prev which takes no parameter but decrements our currentIndex by 1 then calls our display function
    ```js
    function prev() {
        currentIndex = currentIndex === 0 ? menu.length - 1 : currentIndex - 1;
        display(menu[currentIndex]);
    }
    ```
    The reason I'm manipulating the value of currentIndex is __that when it increases it fetch the data from the  next array ___

1.  In similar fashion, I also created a function called next with similar logic.
    ```js
    function next() {
        currentIndex = currentIndex === menu.length - 1 ? 0 : currentIndex + 1;
        display(menu[currentIndex]);
    }
    ```

1.  Next I added some click event listeners to both next and previous buttons
    ```js
    prevmenu.addEventListener("click", prev);
    nextmenu.addEventListener("click", next);
    ```
    The reason for adding click event handlers is so that __when the buttons are clicked it perfotms the function next or prev___

1.  Finally, I _____call my getMenu function to display my arrays__ values
    ```js
    getMenu();
    ```

# Reflection
## What is the hardest part of creating this web app?
- _________________________________

## What remaining JS concepts are still kind of foggy?
- ______________________________________

## Deck of cards API (remnant of Assignment 4)
Given the documentation listed here: https://deckofcardsapi.com/ it lists 2 APIs/REST endpoints `Shuffle the Cards` and `Draw a card`.  What would you need to do to draw 1 card?
- ________________________________________

