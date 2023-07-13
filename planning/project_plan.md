# Project Plan

Pod Members: ** Roy Delgado, Jordan Ward, Anaya Bussey**

## Problem Statement and Description

Insert the latest summary of your problem statement and app description.

### Problem Statement:

We struggle to quickly and accurately assess our company's financial health due to the lack of real-time financial data.

The process of compiling financial reports is time-consuming, leaving little time for analysis.

We lack a centralized location for key financial metrics, leading to disconnected decision-making processes.

We're struggling to understand the impact of different business areas on our financial performance due to disparate data sources.

I'm having trouble keeping track of all my income and expenses. I need a centralized place where I can see everything in one go.

I struggle to set and maintain a budget. I need a tool that can help me set realistic budget goals and track my progress.

I find it hard to visualize my spending patterns. I need a tool that can present my financial data in an easy-to-understand way.

I frequently forget to pay bills on time. I need a system that reminds me when payments are due.

### Description

A financial application that features a Financial dashboard and Personal Finance Management.

Financial Dashboard: Fetches and displays real-time data, including stock prices, Forex rates, commodity prices, and other relevant financial data. Including features like portfolio management, personalized notifications, and trend analysis.

Personal Finance Management: Helps users to track their income and expenses, set budget goals, visualize their spending patterns, and offer suggestions for better money management. Include features like bill reminders, debt tracking, savings goals, etc.

## User Roles and Personas

Include the most up-to-date user roles and personas.

### User Role

1. User

### User Peronas

- User
  
1. A woman, 65 years old, is using this website to help set goals for her spending since she got a large 401K.
   
2. A teenager, 14 years old, is using the site to learn about spending habits and maintain a good financial standing to avoid going over budget

## User Stories

List the current user stories you will implement.

1. As a user, I want to be able to connect my investment accounts to the app, so I can monitor my portfolio in real-time from one platform.
2. As a user, I need to track my different income sources and the expenses related to each project, so I can understand my profitability better.
3. As a user, I would like the app to notify me about significant changes in stock prices or Forex rates that I am interested in, so I can make informed decisions about my investments.
4. As a user, I want to have a feature that automatically categorizes my expenses, so I can easily visualize my spending patterns.
5. As a user, I want to set budget goals for different categories (like groceries, utilities, etc.), so I can manage my household finances more effectively.
6. As a user, I need the app to remind me about my upcoming bill payments, so I never miss a payment and avoid late fees.
7. As a user, I want to use the app to track my progress towards my children's college fund and retirement savings goals, so I can make adjustments if I'm falling behind.
8. As a user, I want the app to provide suggestions on where I can cut back on my spending, so I can save more towards my financial goals.
9. As a user, I need a way to track my debt and visualize how long it will take me to be debt-free based on my current payments, to help me stay motivated.
10. As a user, I want the app to show a comprehensive trend analysis of the financial market, so I can consider investing part of my income in stocks or other commodities.

## Pages/Screens

List all the pages and screens in the app. Include wireframes for at least 3 of them.

Login
Registration
Landing page
Portfolio Page
- Side navbar
-   Dashboard
-   My Goals
-   My Bills
-   Ask For Help
Stock Page
- Side navbar
-  Dashboard
-  My Stocks
-  Watchlist

## Data Model

Describe your app's data model using diagrams or tables

USERS:
id
SERIAL PRIMARY KEY
email
TEXT NOT NULL (contains @)
username
TEXT NOT NULL
firstName
TEXT NOT NULL
lastName
TEXT NOT NULL
password
TEXT NOT NULL
confirmPassword
TEXT NOT NULL (must equal password)


STOCKS/WATCHLIST:
stockID
SERIAL PRIMARY KEY
userID
INT NOT NULL
tickerSymbol
TEXT NOT NULL
Company Name
TEXT NOT NULL
stockPrice
INT NOT NULL
quantity
INT NOT NULL
last_price 
INT NOT NULL
market_cap
INT NOT NULL
exchange 
INT NOT NULL
last_date
DATE

EXPENSE:
expenseID
SERIAL PRIMARY KEY
userID
INT NOT NULL
purchaseName
TEXT NOT NULL
purchaseDescription
TEXT NOT NULL
purchasePrice
INT NOT NULL
purchaseDate
DATE NOT NULL
category
TEXT



GOALS:
goalID
SERIAL PRIMARY KEY
userID
INT NOT NULL
goal_name
TEXT NOT NULL
goal_description
TEXT NOT NULL
target
INT NOT NULL
date_created
DATE NOT NULL
date_due
DATE NOT NULL
type
TEXT NOT NULL


BILLS
billID
SERIAL PRIMARY KEY
userID
INT NOT NULL
bill_name
TEXT NOT NULL
due
DATE NOT NULL
status
BOOL NOT NULL
price
INT NOT NULL


HELP:
helpID
SERIAL PRIMARY KEY
userID
INT NOT NULL
question
TEXT NOT NULL
answer
TEXT NOT NULL



## Endpoints

List the API endpoints you will need to implement.

Name
CRUD
HTTP Verb
Description
User Story

/login
CREATE
POST
Allow the user to log into an existing account
As a user,I want to log into my Financial Dashboard and Personal Finance Management account. 

/register
CREATE
POST
Create an account for an unregistered user
As a user, I want to register for an account 

/stocks
READ
GET
View the list of the users favorited and viewable stocks
As a user, I want see all of my stocks

/expense
READ
GET
View the user’s recent added purchases and expenses
As a user, I want to view my expenses

/stocks
CREATE
POST
Fetch a new stock that the user is interested in viewing on their portfolio dashboard
As a user I want to add a stock

/expense
CREATE
POST
Add a new purchase into the dashboard that includes name, desc, price, and date
As a user I want to add a purchase to my expenses

/watchlist
READ
GET
Allows users to view the stats for stocks they are interested 
As a user, I want to view all of my stocks in the watchlist

/watchlist
CREATE
POST
Allows users to add stocks they are interested in to their watchlist.
As a user, I want to add a stock to my watchlist

/bills
READ
GET
View the list of bills created by the user along with their status of either paid or not paid.
As a user, I would like to view all of my upcoming bills I have yet to pay

/bills
CREATE
POST
Add a new bill to the users list along with the date due, description, and total cost.
As a user I would like to add a bill I have yet to pay and need a reminder of

/goals
READ
GET
Fetch the list of created goals and targets set by the user
As a user I would like to have a view of my goals that I added that I have yet to complete

/goals
CREATE
POST
Add onto the collection of goals that includes the name of the goal, a short description, a target amount, type of goal, and due date.
As a user, I would like to add a goal to my goal list




***Don't forget to set up your Issues, Milestones, and Project Board!***
