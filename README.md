# Hotel-Booking-Analysis-Dashboard
# Overview
The Hotel Booking Analysis Dashboard is a Power BI project that analyzes hotel booking data to provide actionable insights into booking trends, revenue performance, cancellations, guest behavior. The dashboard enables hotel managers and stakeholders to monitor key performance indicators (KPIs) and make data-driven business decisions.

# Content
- Data Source
- Busisness Terminology
- DAX Formulas
- Dashboard
- Analysis and Conclusion

# Data Source
-Dataset: Hotel Booking Demand Dataset
-Source: https://www.kaggle.com/datasets/mojtaba142/hotel-booking/data

# Business Terminology
The dashboard uses several hospitality industry metrics:
- **ADR** : Average Daily Rate (Calculated by dividing the sum of all lodging transactions by the total number of staying.
- **Lead Time** : Number of days that elapsed between the entering date of the booking into the PMS and the arrival date.
- **Length of Stay** : Number of Days that customer stay.
- **Special Requests** : Number of special requests made by the customer (e.g. twin bed or high floor)
- **Repeated Guest** : A customer who has previously stayed at the hotel and made another booking.

# DAX Formulas
DAX measure For KPIs
  * **Total Bookings** : Total Number of Bookings.
    * Formulas : `Total Bookings = COUNTROWS(hotel_booking)`
  * **Total Revenue** : Total revenue generated from confirmed
    * Formulas : `Total Revenue = CALCULATE(SUMX(hotel_booking,hotel_booking[adr] * hotel_booking[Total Nights]),hotel_booking[is_canceled] = 0)`
  * **Cancellation Rate** : Percentage of all bookings that were cancelled.
    * Formulas : `Cancellation Rate (%) = DIVIDE(CALCULATE(COUNTROWS(hotel_booking),hotel_booking[is_canceled] = 1),COUNTROWS(hotel_booking),0)`
  * **Average Lead Time** : Average number of days between the booking date and the guest's arrival date.
    * Formulas : `Average Lead Time = AVERAGE(hotel_booking[lead_time])`
  * **Average ADR**: Average Daily Rate.
    * Formulas : `Average ADR = AVERAGE(hotel_booking[adr])`
  * **Repeated Guess Rate(%)** : Percentage of bookings made by returning (repeat) guests.
    * Formulas : `Repeat Guess Rate (%) = DIVIDE(CALCULATE(COUNTROWS(hotel_booking),hotel_booking[is_repeated_guest] = 1),COUNTROWS(hotel_booking),0)`
  * **Average Length of Stay** : Average total number of nights stayed per booking, including both weekdays and weekends.
    * Formulas : `Average Length of Stay = AVERAGE(hotel_booking[stays_in_week_nights]) + AVERAGE(hotel_booking[stays_in_weekend_nights])`
  * **Total Cancelled Booking** : Total number of bookings that were cancelled.
    * Formulas : `Total Cancelled Booking = CALCULATE(COUNTROWS(hotel_booking),hotel_booking[is_canceled] = 1)`
  * **Revenue Lost** : Total revenue lost due to cancelled bookings.
    * Formulas : `Revenue Lost = CALCULATE(SUMX(hotel_booking,hotel_booking[adr] * hotel_booking[Total Nights]),hotel_booking[is_canceled] = 1)`
  * **Average Guess Per Booking** : Average number of guests per confirmed (non-cancelled) booking.
    * Formulas : `Avg Guests Per Booking = CALCULATE(AVERAGE(hotel_booking[Total Guests]),hotel_booking[is_canceled] = 0)`
  * **Average Special Requests** : Average number of special requests made per confirmed (non-cancelled) booking.
    * Formulas : `Avg Special Requests = CALCULATE(AVERAGE(hotel_booking[total_of_special_requests]),hotel_booking[is_canceled] = 0)`

# Dashboard
This Dashboard containt 3 parts
- **Overview**
- **Cancellation Analysis**
- **Customer Behavior**

**Overview**

**Cancellation Analysis**

**Customer Behavior**



