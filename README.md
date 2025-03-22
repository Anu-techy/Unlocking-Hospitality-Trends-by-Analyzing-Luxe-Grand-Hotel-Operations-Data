# Data Insights of Luxe Hotel Operations

**Aim:** 

To conduct a thorough data analysis of Luxe's operations data and stay competitive while making data-informed decisions

**Steps**

Understanding Business problem

Data Collection and Understanding

Data Cleaning and Exploration

Data Transformation

Collecting insights

===========================================================================

Business Model

Luxe is a 20 year old hotel chain which operates in four cities of India Delhi, Mumbai, Bangalore and Hyderabad.

They have the following types of properties under **Business** and **luxury** category:

1. Luxe Grands 
2. Luxe Exotica
3. Luxe City
4. Luxe Blu
5. Luxe Bay
6. Luxe Palace
7. Luxe Seasons
   
These hotels have the following **room classes**:
   
1. Standard
2. Elite
3. Premium
4. Presidential
  
Hotel bookings can be done from various **booking platforms**  like the company's website, 3rd party booking websites or direct offline.

**booking_status** are Checked Out, Cancelled, No Show         

===========================================

**Data Collection and Understanding**

Data is extracted from Compay's Datawarehouse

**dim_date.csv**           

   Shape:  (92,4)    
   Columns: date, mmmyy, weekno, day_type (weekday/weekend)
   
**dim_hotels.csv**

   Shape:  (25,4)    
   Columns: property_id, property_name, category, city 

**dim_rooms.csv**

   Shape:  (4,2)    
   Columns: room_id, room_class

**fact_aggregated_bookings.csv**

   Shape:  (9200, 5)
   Columns: property_id, check_in_date, room_category, successful_bookings, capacity

**fact_bookings.csv**

   Shape:  (134590, 12)
   Columns: booking_id, property_id, booking_date, check_in_date, checkout_date, no_guests, room_category, 
   booking_platform, ratings_given (1-5), booking_status, revenue_generated, revenue_realized

**new_data_august.csv**

   Shape:  (7, 13)
   Columns: property_id, property_name, category, city, room_category, room_class, check_in_date, mmm yy, 
   week no, day_type, successful_bookings, capacity, occ%

The **occupancy percentage** (often called occ%) measures how many of the hotel's available rooms were actually sold and occupied.

               occ%)} =  (Rooms Sold / Total Rooms Available) * 100

   
