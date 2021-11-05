Original App Design Project - README Template
===  

# Pricey

## Table of Contents
1. [Overview](#Overview)
1. [Product Spec](#Product-Spec)
1. [Wireframes](#Wireframes)
2. [Schema](#Schema)

## Overview
### Description
A price comparer that lets you compare prices of items. Might have to stick to 1 category (like let’s say household items) only because I’m not so sure if the API I researched can look at any item, but the whole point is to help people that may want to just find their cheapest option.

### App Evaluation
[Evaluation of your app across the following attributes]
- **Category:** Social Networking / Saving / Shopping
- **Mobile:** This app would be primarily developed for mobile, can then later on be presented as a website. Functionality would be limited to iPhone users (IOS version may vary).
- **Story:** Why should we have to pay $60+ for jeans, when we can get the exact same pair for less? Everyone love's shopping and saving money at the same time. This app does just that 
- **Market:** Any individual could choose to use this app. It's a safe enviornment. Age might be required if you want to buy things online, among other things. 
- **Habit:**This app could be used as often or unoften as the user wanted depending on how long they want to search for, other things they want to look into, etc...
- **Scope:** First we would start with searches about certain items, then present the user with the same or similar items at a lower price and where they can buy it.

## Product Spec

### 1. User Stories (Required and Optional)

**Required Must-have Stories**

* User can create a new account to save previous searches
* User can login
* User can compare prices of 1 item in various stores that have the product 
* User can save these item prices if they are logged in
* User can logout once they're done

**Optional Nice-to-have Stories**

* User can click on a link to take them to the store they choose to pick 
* User doesn't need to have an account to use the price comparer.
* User can look up stores closest to them if they choose proximity > price.

### 2. Screen Archetypes

* Login Screen
    * User can login
* Create Account Screen
    * User can create an account
* Search Screen
    * User can compare prices of 1 item in various stores that have the product
* Logout Screen
    * User can logout once they're done
* Map Locator Screen
    * User can see where the 
* Stores Screen
    * User can view the stores that have the item they want

### 3. Navigation

**Tab Navigation** (Tab to Screen)

* Compare Price
* Location of stores
* Stores (with the items in stock)

**Flow Navigation** (Screen to Screen)

* Login Screen
    * Search
    * Stores
    * Map Locator
* Create Account Screen
    * Search
    * Stores
    * Map Locator
* Search Screen
    * Stores
* Logout Screen
    * Login
* Map Locator Screen
    * Stores
    * Search
* Stores Screen
    * Search
    * Map Locator

## Wireframes

![](https://i.imgur.com/1sKrO53.jpg)


## Schema 
### Models
|  Property  |    Type     |        Description          |
|  --------  |    ------   |        -----------          |
|  price     |    Number   |price of the object desired  |
|  product   |    String   |the object that user wants to look for/buy|
|  email     |    String   |user's email that will be used to identify identity upon creation of account|
|  Image     |    File     |an image of the user's searched product|

### Networking
- [Add list of network requests by screen ]
- [Create basic snippets for each Parse network request]
- [OPTIONAL: List endpoints if using existing API such as Yelp]
