# Hotel-Booking-Analysis
This project contains the real world data record of hotel bookings of a City and a Resort hotel containing details like bookings, cancellations, guest details etc. from 2015 to 2017. Main aim of the project is to understand and visualize dataset from hotel and customer point of view.

![Hotel-Booking-1280x720](https://user-images.githubusercontent.com/112092937/224477789-656e55f2-cc79-4382-8b8a-33d11df38103.jpg)

# Objective
Out main objective is perform EDA on the given dataset and draw useful conclusions about general trends in hotel bookings and how factors governing hotel bookings interact with each other.

# Dataset
This dataset contains booking information for a city hotel and a resort hotel. It contains the following features.
- hotel: Name of hotel ( City or Resort)
- is_canceled: Whether the booking is canceled or not (0 for no canceled and 1 for canceled)
- lead_time: time (in days) between booking transaction and actual arrival.
- arrival_date_year: Year of arrival
- arrival_date_month: month of arrival
- arrival_date_week_number: week number of arrival date.
- arrival_date_day_of_month: Day of month of arrival date
- stays_in_weekend_nights: No. of weekend nights spent in a hotel
- stays_in_week_nights: No. of weeknights spent in a hotel
- adults: No. of adults in single booking record.
- children: No. of children in single booking record.
- babies: No. of babies in single booking record. 
- meal: Type of meal chosen 
- country: Country of origin of customers (as mentioned by them)
- market_segment: What segment via booking was made and for what purpose.
- distribution_channel: Via which medium booking was made.
- is_repeated_guest: Whether the customer has made any booking before(0 for No and 1 for 
                     Yes)
- previous_cancellations: No. of previous canceled bookings.
- previous_bookings_not_canceled: No. of previous non-canceled bookings.
- reserved_room_type: Room type reserved by a customer.
- assigned_room_type: Room type assigned to the customer.
- booking_changes: No. of booking changes done by customers
- deposit_type: Type of deposit at the time of making a booking (No deposit/ Refundable/ No refund)
- agent: Id of agent for booking
- company: Id of the company making a booking
- days_in_waiting_list: No. of days on waiting list.
- customer_type: Type of customer(Transient, Group, etc.)
- adr: Average Daily rate.
- required_car_parking_spaces: No. of car parking asked in booking
- total_of_special_requests: total no. of special request.
- reservation_status: Whether a customer has checked out or canceled,or not showed 
- reservation_status_date: Date of making reservation status.

Total number of rows in data: 119390

Total number of columns: 32

# Data Cleaning and Feature Engineering
## (1) Removing Duplicate rows

All duplicate rows were dropped.

## (2) Handling null values

Null values in columns company and agent were replaced by 0.

Null values in column country were replaced by mode.

Null values in column children were replaced by the mean of the column.

## (3) Converting columns to appropriate data types

Changed data type of children, company, agent to int type.

Changed data type of reservation_status_date to date type.

## (4) Creating new columns

Created new column total_stay by adding stays_in_weekend_nights+stays_in_week_nights.

Created new column total_people by adding adults+children+babies.


# Exploratory Data Analysis

Performed EDA and tried answering the following questions:
1) Which year have a more number of bookings?
2) How many bookings are done in every year according to the hotel?
3) What is the booking cancellation ratio?
4) Which hotel has higher bookings cancellation rate?
5) Which month has maximum bookings?
6) Which agent does the most bookings?
7) Which agent has the lowest booking cancellation ratio?
8) Which distribution channel has highest booking rate?
9) Which distribution channel has highest cancellation percentage?
10) Which type of deposit is preferred by customers?
11) Which type of food(meal) is preferred by customers?
12) Which country has the highest number of bookings by customers?
13) Which is the most booked accommodation type (Single, Couple, Family)?
14) Which type of room is most in demand?
15) How many nights guests choose to stay the hotel?
16) What is the ratio of repeated guest?
17) Which month has the highest ADR (Hotel wise)?
18) What is the average ADR of hotel?
19) By which market segment are the most bookings done?
20) Which market segment has the longest lead time?
21) Relationship between number of Total Stay and ADR.
22) Correlation between two parameters.


# Conclusion
- Overall ADR of City hotel is slightly higher than Resort hotel. 
- Mostly guests stay for less than 4 nights in hotel and for longer stays they preferred Resort 
hotel.
- 4% of visitors return for another booking at the City Hotel, and 6% of visitors return to the 
Resort hotel for another stay.
- Europeans and Portuguese are the majority of guests.
- Mostly preferred channel for booking is TA/TO
- Booking cancellation ratio in TA/TO is 30%
- July- August are the busier and most profitable months for both of hotels. 
- Couples are the most common guests for hotels; hence hotels can plan services according to 
couples needs to increase revenue.
- Low ADR for longer stays (more than 15 days)
- Booking cancellation ratio - 27.5%.
- Agent 9 is done more number of bookings while Agent 464 has lowest cancellation ratio.
- When it comes to longer stays in hotel, guest do plan much in advance

# Dashboard - Hotel Booking Analysis


https://tabsoft.co/3ENdskX

![Screenshot_20230301_215229](https://user-images.githubusercontent.com/112092937/222200217-03a8db28-48b7-4922-9f24-9acb8851b6d1.png)


