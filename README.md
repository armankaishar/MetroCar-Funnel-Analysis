# Funnel Analysis Mastery Project

> This project aims to analyze the customer funnel of Metrocar, a ride-sharing app (similar to Uber/Lyft), to identify areas for improvement and optimization. We will use SQL for data collection and Pandas for further analysis and visualisation. The stakeholders have asked several business questions that can uncover valuable insights for improving specific areas of the customer funnel. Your task is to conduct a funnel analysis and present your analysis and recommendation. Explain your reason for your recommendation based on insights retrieved from the data. 

## Project Background

🚗 About Metrocar
Metrocar's business model is based on a platform that connects riders with drivers through a mobile application. Metrocar acts as an intermediary between riders and drivers, providing a user-friendly platform to connect them and facilitate the ride-hailing process.
 
notion image
 
📶 Metrocar’s Funnel

The customer funnel for Metrocar typically includes the following stages:

App Download: A user downloads the Metrocar app from the App Store or Google Play Store.

Signup: The user creates an account in the Metrocar app, including their name, email, phone number, and payment information.

Request Ride: The user opens the app and requests a ride by entering their pickup location, destination, and ride capacity (2 to 6 riders).

Driver Acceptance: A nearby driver receives the ride request and accepts the ride.

Ride: The driver arrives at the pickup location, and the user gets in the car and rides to their destination.

Payment: After the ride, the user is charged automatically through the app, and a receipt is sent to their email.

Review: The user is prompted to rate their driver and leave a review of their ride experience.

Similar to other customer funnels, there will be drop-offs at every stage of the funnel, which is why funnel analysis can be helpful in identifying areas for improvement and optimization. For example, Metrocar may analyze the percentage of users who download the app but do not complete the registration process, or the percentage of users who request a ride but cancel before the driver arrives.
 
🔎 Business questions

You will need to analyze the data and make recommendations based on the following business questions:

What steps of the funnel should we research and improve? Are there any specific drop-off points preventing users from completing their first ride?

Metrocar currently supports 3 different platforms: ios, android, and web. To recommend where to focus our marketing budget for the upcoming year, what insights can we make based on the platform?

What age groups perform best at each stage of our funnel? Which age group(s) likely contain our target customers?

Surge pricing is the practice of increasing the price of goods or services when there is the greatest demand for them. If we want to adopt a price-surging strategy, what does the distribution of ride requests look like throughout the day?

What part of our funnel has the lowest conversion rate? What can we do to improve this part of the funnel?

The Dataset

This dataset is inspired by publicly available datasets for Uber/Lyft. The data for this dataset was generated specifically for this project.
Connect to the Metrocar database

Copy the following URL to use with sqlalchemy and Pandas:

postgresql://Test:bQNxVzJL4g6u@ep-noisy-flower-846766-pooler.us-east-2.aws.neon.tech/Metrocar
Connect to the Metrocar database

Copy the following URL to use with sqlalchemy and Pandas:

postgresql://Test:bQNxVzJL4g6u@ep-noisy-flower-846766-pooler.us-east-2.aws.neon.tech/Metrocar
 
Dataset structure
You can find a description of each table and its columns below.
app_downloads: contains information about app downloads
app_download_key: unique id of an app download
platform: ios, android or web
download_ts: download timestamp
signups: contains information about new user signups
user_id: primary id for a user
session_id: id of app download
signup_ts: signup timestamp
age_range: the age range the user belongs to
ride_requests: contains information about rides
ride_id: primary id for a ride
user_id: foreign key to user (requester)
driver_id: foreign key to driver
request_ts: ride request timestamp
accept_ts: driver accept timestamp
pickup_location: pickup coordinates
destination_location: destination coordinates
pickup_ts: pickup timestamp
dropoff_ts: dropoff timestamp
cancel_ts: ride cancel timestamp (accept, pickup and dropoff timestamps may be null)
transactions: contains information about financial transactions based on completed rides:
ride_id: foreign key to ride
purchase_amount_usd: purchase amount in USD
charge_status: approved, cancelled
transaction_ts: transaction timestamp
reviews: contains information about driver reviews once rides are completed
review_id: primary id of review
ride_id: foreign key to ride
driver_id: foreign key to driver
user_id: foreign key to user (requester)
rating: rating from 0 to 5
free_response: text response given by user/requester



### Key Requirements

Format
Criteria
Meets Specification
Submission is through the designated form
- Submission form will include the links to a colab notebook (or uploaded .ipynb-file, with outputs) and presentation recording, uploaded presentation.
Video presentation is the appropriate format
- Video is 3-5 minutes long.
- Video includes the speaker view.
- Presentation uses slides, included as a PDF file.
Use specified tools
- Get data from database using sqlalchemy & Pandas.
- Analyse data using pandas.
- Visualise your findings using matplotlib, seaborn and/or plotly.
Funnel Analysis
Criteria
Meets Specification
Funnel Visualization
- Create funnel visualizations that adequately represent the different stages of the funnel analysis.
Insights and Recommendations
- Provide meaningful insights and reasonable recommendations based on the funnel analysis.
- Support recommendations based on evidence extracted from the data.
Specificity
- Drill-down into one or two specific sections of the funnel.
- Extract meaningful insights within these sections citing areas of opportunity to either increase or reduce marketing spend, product feature development, etc.
Visualize these findings!
Data Storytelling
Criteria
Meets Specification
Presentation is optimized for the audience and format
- Presentation caters to a non-technical audience. Overly technical statistical language and unnecessary analysis details are avoided.
- Slides have a clear takeaway stated in the title or bullet points.
- Slides don’t include too much text (over 250 characters or so). Voiceover in the presentation explains the nuances and details.
- Each slide does not include more than 1-2 charts. Any included charts are clearly tied to the takeaway.
Charts follow the visualization best practices
- Each chart type (bar, line, histogram, etc) should be appropriate for the data type and desired takeway.
- Charts have clear titles, axis labels, and axis tick labels.
- Charts make minimal and appropriate use of color.
