# Hotel-Booking-Analysis-Dashboard
# Overview
The Hotel Booking Analysis Dashboard is a Power Bi Project 

# Content
- Introduction to Dataset
- DAX Formulas
- Dashboard
- Analysis and Conclusion

# Introduction and Data Source
data source: https://www.kaggle.com/datasets/mojtaba142/hotel-booking/data 
This part explain hotel technical term
- **ADR** stand for Average Daily Rate 
- **Lead Time** stand for 

# DAX Formulas
*KPI Formulas
  * **Total Bookings** : Total Number of Bookings.
    * Formulas : `Total Bookings = COUNTROWS(hotel_booking)`
  * **Total Revenue** :
    * Formulas : `Total Revenue = CALCULATE(SUMX(hotel_booking,hotel_booking[adr] * hotel_booking[Total Nights]),hotel_booking[is_canceled] = 0)`
  * **Cancellation Rate** :
    * Formulas : `Cancellation Rate (%) = DIVIDE(CALCULATE(COUNTROWS(hotel_booking),hotel_booking[is_canceled] = 1),COUNTROWS(hotel_booking),0)`
  * **Average Lead Time** :
    * Formulas : Average Lead Time = AVERAGE(hotel_booking[lead_time])
  * **Average ADR**:
    * Formulas :
  * **Repeated Guess Rate(%)** :
    * Formulas :
  * **Avergae Length of Stay** :
    * Formulas :
  * **Total Cancelled Booking** :
    * Formulas :
  * **Revenue Lost** :
    * Formulas :
  * **Average Guess Per Booking** :
    * Formulas :
  * **Average Special Requests** :
    * Formulas :
   
