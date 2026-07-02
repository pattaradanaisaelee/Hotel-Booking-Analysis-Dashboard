# Hotel-Booking-Analysis-Dashboard
# Overview
The Hotel Booking Analysis Dashboard is a Power Bi Project 



# Content
- Introduction to Dataset
- DAX Formulas
- Dashboard
- Analysis and Conclusion

# Introduction to Dataset
data source: https://www.kaggle.com/datasets/mojtaba142/hotel-booking/data 
This part explain hotel technical term
- **ADR** stand for Average Daily Rate 
- **Lead Time** stand for 

# DAX Formulas
This part containt 2 separate part. Measure DAX and Columns DAX
- Measure DAX
  * **Total Bookings** : Total Number of Bookings
    * Formulas : `Total Bookings = COUNTROWS(hotel_booking)`
  * **Total Revenue** :
    * Formulas : `Total Revenue = CALCULATE(SUMX(hotel_booking,hotel_booking[adr] * hotel_booking[Total Nights]),hotel_booking[is_canceled] = 0)`
  * **Cancellation Rate**:
  * * Formulas : `Cancellation Rate (%) = DIVIDE(CALCULATE(COUNTROWS(hotel_booking),hotel_booking[is_canceled] = 1),COUNTROWS(hotel_booking),0)`
