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

- [x]  User can create a new account to save previous searches

- [x]  User can login

- [x] User can compare prices of 1 item in various stores that have the product 
- [x] User can save these item prices if they are logged in
 User can logout once they're done

**Optional Nice-to-have Stories**

* User can click on a link to take them to the store they choose to pick 
- [x] User doesn't need to have an account to use the price comparer.
* User can look up stores closest to them if they choose proximity > price.

### 2. Screen Archetypes

* Login Screen
   - [x] User can login
* Create Account Screen
   - [x] User can create an account
* Search Screen
   - [x] User can compare prices of 1 item in various stores that have the product
* Logout Screen
    * User can logout once they're done
* Map Locator Screen
    * User can see where the 
* Stores Screen
    * User can view the stores that have the item they want

### 3. Navigation

**Tab Navigation** (Tab to Screen)

- [x] Compare Price
* Location of stores
- [x] Stores (with the items in stock)

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


## Video Walkthrough

## Update 3

![codepath22](https://user-images.githubusercontent.com/67729867/143729863-0f483613-74ec-4895-a669-4ae61523136f.gif)

## Update 2

![ezgif com-gif-maker(1)](https://user-images.githubusercontent.com/67729867/142714725-d4fae368-1c0b-4e36-8833-44d317bc5b08.gif)

<img width="231" alt="codepath" src="https://user-images.githubusercontent.com/67729867/142714779-51ff8d7b-cddc-482d-a3d1-8730c2d04daa.png">


## Update 1
![](https://i.imgur.com/G9vQ5w9.gif)


## Schema 
### Models
Looking up price:

|  Property  |    Type     |        Description          |
|  --------  |    ------   |        -----------          |
|  price     |    Number   |price of the object desired  |
|  product   |    String   |the object that user wants to look for/buy|
|  email     |    String   |user's email that will be used to identify identity upon creation of account|
|  Image     |    File     |an image of the user's searched product|
|  password  |    String   |authentication to log in to user's account |
|  storeCount|    Number   |keeps track of how many stores were found with the product in stock|


### Networking
* Login Screen
   * (READ/GET): will get the inputted email and password and login user if correct combo
   * (UPDATE/PUT): will be updating user table to add a new user when requesting creation of new account
* Search Screen 
   * (GET/search): This endpoint is used to search the product from the stores
``` python {
    "data": [
        {
            "product_title": "Apple iPhone 6 32GB",
            "can_compare": true,
            "product_lowest_price": 26490,
            "product_link": "https://price-api.datayuge.com/api/v1/compare/detail?id=ZToxMjIyNA",
            "product_id": "ZToxMjIyNA",
            "product_category": "mobile",
            "product_sub_category": "mobile",
            "product_image": "http://images-api.datayuge.in/image/MTIyMjQtMjYtMQ.jpg"
        }, 
   ```
* Stories Screen 
   * GET /detail: This resource will the detailed about the product. It may include the basic product details, images, colour options and pricing from different stores
``` python {
    "data": {
        "product_name": "Apple iPhone 6 32GB",
        "product_model": "iPhone 6 32GB",
        "product_brand": "Apple",
        "product_id": "ZToxMjIyNA",
        "product_ratings": "4.2",
        "product_category": "mobile",
        "product_sub_category": "mobile",
        "is_available": true,
        "available_colors": [
            "All Colours",
            "Gold",
            "Grey",
            "Silver"
        ], 
```
   * GET /list: this resource will show all the products in a particular category. 
``` python {
    "data": [
        {
            "product_title": "Xiaomi Redmi 4A",
            "can_compare": true,
            "product_lowest_price": 5998,
            "product_link": "https://price-api.datayuge.com/api/v1/compare/detail?id=ZToxMTYwNQ",
            "product_id": "ZToxMTYwNQ",
            "product_category": "mobile",
            "product_sub_category": "mobile"
        },
        {
            "product_title": "Xiaomi Redmi 4",
            "can_compare": true,
            "product_lowest_price": 6998,
            "product_link": "https://price-api.datayuge.com/api/v1/compare/detail?id=ZToxMTE0Ng",
            "product_id": "ZToxMTE0Ng",
            "product_category": "mobile",
            "product_sub_category": "mobile"
        },
```
   
   * GET /price: Displays price without calling the whole function 
  
 ```python {
    "amazon": "28490",
    "flipkart": "28990",
    "snapdeal": "",
    "ebay": "29499",
    "paytm": "",
    "croma": "27999",
    "yebhi": "",
    "indiatimes": "",
    "homeshop18": "",
    "naaptol": "",
    "infibeam": "28095",
    "tatacliq": "27999",
    "shopclues": "29499"
}
```
