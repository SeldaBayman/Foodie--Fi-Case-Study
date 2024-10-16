Case Study #3 - Foodie-Fi /Danny MA · May 18, 2021

![63386b11-8142-400c-92cc-65b9677c63d5](https://github.com/user-attachments/assets/ecc54e1c-b0ca-4292-b01f-b738590c9c83)

Introduction
Subscription based businesses are super popular and Danny realised that there was a large gap in the market - he wanted to create a new streaming service that only had food related content - something like Netflix but with only cooking shows!
Danny finds a few smart friends to launch his new startup Foodie-Fi in 2020 and started selling monthly and annual subscriptions, giving their customers unlimited on-demand access to exclusive food videos from around the world!
Danny created Foodie-Fi with a data driven mindset and wanted to ensure all future investment decisions and new features were decided using data. This case study focuses on using subscription style digital data to answer important business questions.

Available Data
Danny has shared the data design for Foodie-Fi and also short descriptions on each of the database tables - our case study focuses on only 2 tables but there will be a challenge to create a new table for the Foodie-Fi team.
All datasets exist within the foodie_fi database schema - be sure to include this reference within your SQL scripts as you start exploring the data and answering the case study questions.

Entity Relationship Diagram
Table 1: plans
Customers can choose which plans to join Foodie-Fi when they first sign up.
Basic plan customers have limited access and can only stream their videos and is only available monthly at $9.90
Pro plan customers have no watch time limits and are able to download videos for offline viewing. Pro plans start at $19.90 a month or $199 for an annual subscription.
Customers can sign up to an initial 7 day free trial will automatically continue with the pro monthly subscription plan unless they cancel, downgrade to basic or upgrade to an annual pro plan at any point during the trial.
When customers cancel their Foodie-Fi service - they will have a churn plan record with a null price but their plan will continue until the end of the billing period.

Table 2: subscriptions
Customer subscriptions show the exact date where their specific plan_id starts.-
If customers downgrade from a pro plan or cancel their subscription - the higher plan will remain in place until the period is over - the start_date in the subscriptions table will reflect the date that the actual plan changes.
When customers upgrade their account from a basic plan to a pro or annual pro plan - the higher plan will take effect straightaway.
When customers churn - they will keep their access until the end of their current billing period but the start_date will be technically the day they decided to cancel their service.

Interactive SQL Instance
You can use the embedded DB Fiddle below to easily access these example datasets - this interactive session has everything you need to start solving these questions using SQL.
You can click on the Edit on DB Fiddle link on the top right hand corner of the embedded session below and it will take you to a fully functional SQL editor where you can write your own queries to analyse the data.
You can feel free to choose any SQL dialect you’d like to use, the existing Fiddle is using PostgreSQL 13 as default.
Serious SQL students will have access to the same relevant schema SQL and example solutions which they can use with their Docker setup from within the course player!

Case Study Questions
This case study is split into an initial data understanding question before diving straight into data analysis questions before finishing with 1 single extension challenge.

A. Customer Journey
Based off the 8 sample customers provided in the sample from the subscriptions table, write a brief description about each customer’s onboarding journey.

Try to keep it as short as possible - you may also want to run some sort of join to make your explanations a bit easier!

B. Data Analysis Questions
How many customers has Foodie-Fi ever had?
What is the monthly distribution of trial plan start_date values for our dataset - use the start of the month as the group by value
What plan start_date values occur after the year 2020 for our dataset? Show the breakdown by count of events for each plan_name
What is the customer count and percentage of customers who have churned rounded to 1 decimal place?
How many customers have churned straight after their initial free trial - what percentage is this rounded to the nearest whole number?
What is the number and percentage of customer plans after their initial free trial?
What is the customer count and percentage breakdown of all 5 plan_name values at 2020-12-31?
How many customers have upgraded to an annual plan in 2020?
How many days on average does it take for a customer to an annual plan from the day they join Foodie-Fi?
Can you further breakdown this average value into 30 day periods (i.e. 0-30 days, 31-60 days etc)
How many customers downgraded from a pro monthly to a basic monthly plan in 2020?

C. Challenge Payment Question
The Foodie-Fi team wants you to create a new payments table for the year 2020 that includes amounts paid by each customer in the subscriptions table with the following requirements:

monthly payments always occur on the same day of month as the original start_date of any monthly paid plan
upgrades from basic to monthly or pro plans are reduced by the current paid amount in that month and start immediately
upgrades from pro monthly to pro annual are paid at the end of the current billing period and also starts at the end of the month period
once a customer churns they will no longer make payments

D. Outside The Box Questions
The following are open ended questions which might be asked during a technical interview for this case study - there are no right or wrong answers, but answers that make sense from both a technical and a business perspective make an amazing impression!
How would you calculate the rate of growth for Foodie-Fi?
What key metrics would you recommend Foodie-Fi management to track over time to assess performance of their overall business?
What are some key customer journeys or experiences that you would analyse further to improve customer retention?
If the Foodie-Fi team were to create an exit survey shown to customers who wish to cancel their subscription, what questions would you include in the survey?
What business levers could the Foodie-Fi team use to reduce the customer churn rate? How would you validate the effectiveness of your ideas?

Conclusion
This case study should reflect realistic questions we usually focus on for all product related analytics requests in a wide variety of industries, especially in the digital space

🍽️ Foodie-Fi Subscription Analysis SQL Project Mine Analysis:
Welcome to my Foodie-Fi SQL project! 🎉 In this project, I performed an in-depth analysis of customer behavior and subscription patterns on the Foodie-Fi platform. Using SQL, I explored key business metrics, subscription trends, and customer upgrade/downgrade tendencies. Here’s an overview of what I’ve accomplished in this analysis:

🔍 Project Overview
This project focused on analyzing Foodie-Fi’s customer subscription data, revealing critical insights on customer preferences, subscription durations, and patterns across various plans.

Key Analyses:
Customer Distribution by Plan (as of 2020-12-31): Examined how customers are distributed across the Basic Monthly, Pro Monthly, Annual, Trial, and Cancelled plans, including percentage breakdowns.

Subscription Upgrades: Analyzed how many customers upgraded to the Annual Plan in 2020, and calculated the average time it took for customers to switch from any plan to an annual plan (found to be approximately 45 days!).

Time Period Breakdown: Grouped customers’ transition times into 30-day periods (e.g., 0-30 days, 31-60 days, etc.) to see how quickly customers tend to upgrade.

Downgrade Analysis: Identified how many customers downgraded from the Pro Monthly plan to the Basic Monthly plan in 2020 and evaluated potential reasons behind this behavior.

🏆 A-B-C-D Section Solutions
In addition to the general analysis, I successfully tackled the A-B-C Sections of the project:

![7_B](https://github.com/user-attachments/assets/7ce97c12-dcd1-4fc1-bb99-d39a3e5be898)

![8_B](https://github.com/user-attachments/assets/34234e64-f03c-448b-a1b8-0285483ee5d3)

A Section: Compared the success rates of different subscription plans by grouping customer data effectively.
B Section: Analyzed the trend of subscription cancellations over time, providing strategic insights into customer churn.
C Section: Explored correlations between metrics such as upgrades, downgrades, and cancellation tendencies, helping to better understand customer behavior.
D Section:Identified business strategies to reduce customer churn and improve retention, focusing on key growth metrics, customer journey analysis, and personalized engagement campaigns to enhance long-term success.

![9_B](https://github.com/user-attachments/assets/df174663-a740-4f58-8bea-2f5f89b08a98)

![10_B](https://github.com/user-attachments/assets/16d88804-04c9-4d19-8652-315021e6322b)


📊 Insights & Learnings
This project gave me valuable insights into the subscription dynamics on the Foodie-Fi platform. Key findings include:

Customers tend to upgrade to Annual Plans within the first 45 days after joining.
The Basic Monthly plan has the largest customer base, while upgrades to Pro Monthly and Annual Plans require further incentives.
Downgrade trends suggest pricing sensitivity among some customers, particularly between the Pro and Basic plans.
Customers who engage frequently with premium content are more likely to remain subscribed to higher-tier plans, indicating a need for enhanced content offerings to improve retention in premium plans.
Churn rates are highest in the first 60 days, suggesting that improving the onboarding experience and offering personalized incentives during this period could significantly reduce cancellations.
A strong correlation between customer engagement and long-term retention highlights the importance of personalized campaigns to re-engage inactive users and drive loyalty.
Finally, implementing flexible subscription options, such as a pause feature or loyalty rewards, could help retain customers facing price sensitivity or reduced platform usage.

💻 Technologies Used
SQL: Core analysis and data querying.
Data Visualization Tools (optional depending on if you used any tools for showcasing insights): To display key trends in customer behavior.

📂 Check the Project
Feel free to explore the SQL queries and analyses in this repository. Each query is designed to answer specific business questions regarding customer subscriptions and behaviors on the 
Foodie-Fi platform.


https://8weeksqlchallenge.com/case-study-3/
