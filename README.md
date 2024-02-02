# 5-1-0 Assignment

**Table of Contents:**
- [Short Response](#short-response)
- [Overview](#overview)
  - [User Stories](#user-stories)
  - [Starting Code](#starting-code)
  - [Your Task:](#your-task)
- [Part 1: Cart Item](#part-1-cart-item)
- [Part 2: Shopping Cart Instance Properties/Methods](#part-2-shopping-cart-instance-propertiesmethods)
- [Part 3: Shopping Cart Class Properties/Methods](#part-3-shopping-cart-class-propertiesmethods)


## Short Response

Do them! There are only 3 questions

## Overview

In this assignment, you will be tasked with completing the data management portion of an application.

![a fruit stand application with an inventory and a cart. users can add items to the cart which shows the total price.](./images/final-app.png)

### User Stories 

Upon completing this assignment, the user should be able to:
* Browse a list of fruits available for purchase
* Click on a fruit to add it to their cart
* See the total price of all items in their cart
* Click on an item in the cart to remove it.

### Starting Code

> Remember to run `npm i` to install the dependencies!

To start this assignment, you will be given a Vite project with all rendering and user event logic implemented for you in the `vite-project` folder! Check out what you are starting with by running `npm run dev` and then browsing through the `src/main.js` file and the `src/utils/` folder.

There are tests available to you through `npm test`. Take time to understand the test and what they are looking for. Understanding the flow of data in the application will also be helpful to test out your code when running application. 

### Before you begin...

**Reminder**: We are using ES Modules!

Because we are using ES Modules and working in the front end, you cannot test your files individually in Node (the terminal in VS code or otherwise). Make sure that you are using the console in the browser when testing your code.

### Your Task:

Your job is to build the two classes:
* `ShoppingCart` in the `src/model/ShoppingCart.js` file
* `CartItem` in the `src/model/CartItem.js` file

Only the `ShoppingCart` class is directly used by the rest of the application (see `src/main.js` and `src/utils/render-functions.js`). However, the `CartItem` class is used by the `ShoppingCart`.

Below you will find requirements for each class which you can test using `npm test`. 

Let's get started! You got this!

## Part 1: Cart Item

The instructions here are intentionally vague. Look at the associated `.spec.js` files to see how we are using your class!

Create a `CartItem` class.

It should have the following instance properties:
- `id`: a unique value generated from the getId helper function
- `name`: the given name of the item
- `price`: the given price of the item

## Part 2: Shopping Cart Instance Properties/Methods

Create a `ShoppingCart` class.

It should have the following **instance properties**:
- `id`: a unique value generated from the getId helper function
- `#cartItems`: a private array of items held by this `ShoppingCart` instance

It should have the following **instance methods**:
- `createItem(name, price)`: creates a new CartItem and adds it to the instance's cart
- `getItems()`: returns the array of items held by this `ShoppingCart` instance
- `removeItem(id)`: removes an item from the instance's cart based on the given id
- `getTotal()`: returns the total price of all itesm held by this `ShoppingCart` instance

## Part 3: Shopping Cart Class Properties/Methods

It should have the following **static class properties**:
- `#allCarts`: a private array of all `ShoppingCart` instances

It should have the following **static class methods**:
- `listAll()`: returns a copy of the array of all `ShoppingCart` instances 
- `findBy(id)`: returns the `ShoppingCart` instance with the given `id`

