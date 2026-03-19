**1. Retrieve all successful bookings**

&nbsp;SELECT \* FROM bookings WHERE Booking\_Status = 'Success';





**2. Find the average ride distance for each vehicle type**

SELECT Vehicle\_Type, AVG(Ride\_Distance) as avg\_distance FROM bookings GROUP BY

Vehicle\_Type;



**3. Get the total number of cancelled rides by customers**

SELECT COUNT(\*) FROM bookings WHERE Booking\_Status = 'cancelled by Customer';





**4. List the top 5 customers who booked the highest number of rides**

SELECT Customer\_ID, COUNT(Booking\_ID) as total\_rides FROM bookings GROUP BY

Customer\_ID ORDER BY total\_rides DESC LIMIT 5;



**5. Get the number of rides cancelled by drivers due to personal and car-related issues**

SELECT COUNT(\*) FROM bookings WHERE cancelled\_Rides\_by\_Driver = 'Personal \& Car

related issue';



**6. Find the maximum and minimum driver ratings for Prime Sedan bookings**

SELECT MAX(Driver\_Ratings) as max\_rating, MIN(Driver\_Ratings) as min\_rating FROM

bookings WHERE Vehicle\_Type = 'Prime Sedan';



**7. Retrieve all rides where payment was made using UPI**

SELECT \* FROMbookings WHERE Payment\_Method = 'UPI';





**8. Find the average customer rating per vehicle type**

SELECT Vehicle\_Type, AVG(Customer\_Rating) as avg\_customer\_rating FROM bookings

GROUPBYVehicle\_Type;



**9. Calculate the total booking value of rides completed successfully**

SELECT SUM(Booking\_Value) as total\_successful\_value FROM bookings WHERE

Booking\_Status = 'Success';



**10. List all incomplete rides along with the reason**

SELECT Booking\_ID, Incomplete\_Rides\_Reason FROM bookings WHERE Incomplete\_Rides =

'Yes';





