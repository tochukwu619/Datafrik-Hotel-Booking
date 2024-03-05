# Datafrik-Hotel-Booking


### PROJECT OVERVIEW

This dataset consists of 66,542 hotel bookings between January 1st, 2010 to December 31st, 2019 from a company who help international travelers around the world secure hotel in destination countries. The goal of the analysis is to develop insight on the booking and revenue trend of the company.
![Datafrik Overview](https://github.com/tochukwu619/Datafrik-Hotel-Booking/assets/125865918/4e420d6c-44b2-41d0-98e8-6a31950d388c)


### DATA SOURCE

The dataset used for this project was gotten from a Datafrik. The file name is ‘Hotel Dataset.xlsx’. Each table contains: origin country, origin states, destination country, destination states, age, gender, room type, check-in and check-out dates, number of room occupant, booking fees, taxes (GST), hotel rating and customers payment methods for the bookings.  

### TOOLS

-	Python
-	Microsoft Power BI
-	Microsoft Excel

### DATA PREPARATION

Using Microsoft Excel, the data was cleaned by ensuring that there were no duplicates. Spelling checks were also performed on the fields for consistency. Blank-value check was done to ensure that there was no inappropriate blank cell. 

### EXPLORATORY DATA ANALYSIS

A full exploratory data analysis was done using a package in python called, y-data_profiling. This report can be seen here - [Full Report]()


### DATA ANALYSIS

Using Microsoft Power BI, a dashboard was developed to provide a visual insight on the key sales metrics. New columns were created for:

Age group
```
Age Group = IF(Hotel_Booking[Age] < 30, "Young Adults(< 30)", IF(Hotel_Booking[Age] < 50, "Adults (< 50)", "Elderly (> 49)"))
```

Earning before tax
```
Earning Before Tax = (Hotel_Booking[Booking Price[SGD]]] * Hotel_Booking[Profit Margin]) + (Hotel_Booking[Booking Price[SGD]]] * Hotel_Booking[Taxes (GST)]) 
```

Lead time
```
Lead Time = DATEDIFF(Hotel_Booking[Date of Booking], Hotel_Booking[Check-in date], DAY)
```

Net income
```
Net Income = (Hotel_Booking[Booking Price[SGD]]] * Hotel_Booking[Profit Margin])
```

While measures were created for:

Total number of guests
```
# Guests = SUM(Hotel_Booking[No. Of People])
```

Average hotel rating
```
Avg Hotel Rating = AVERAGE(Hotel_Booking[Hotel Rating]) 
```

Average lead time for booking
```
Avg Lead Time = AVERAGE(Hotel_Booking[Lead Time])
```

Average length of stay
```
Avg Length of Stay = AVERAGE(Hotel_Booking[Number of Days])
```

Maximum hotel rating
```
Max Hotel Rating = 5
```

Maximum lead time
```
Max Lead Time = 100
```

Maximum length of stay
```
Max Length of Stay = 97
```

Minimum hotel rating
```
Min Hotel Rating = 0
```

Minimum lead time
```
Min Lead Time = 1 
```

Minimum length of stay
```
Min Length of Stay = 1
```

Count of bookings
```
Total Booking = COUNT(Hotel_Booking[Booking ID])
```

Revenue from bookings
```
Total Booking Price = SUM(Hotel_Booking[Booking Price[SGD]]]) 
```

Total earnings before tax
```
Total Earning Before Tax = SUM(Hotel_Booking[Earning Before Tax])
```

Net income
```
Total Net Income = SUM(Hotel_Booking[Net Income])
```


### RESULTS/FINDING

-	It was observed that an error was made in one of the values in the age column (-5). This was filtered out when using the age column for any analysis.
-	It was observed that the top 2 destination countries are: New Zealand (3,447) and Nepal (3,446).
-	The top for bookings were made from: Thailand (12,170), Malaysia (12,049), Singapore (12,037), Indonesia (11,986).
-	There was a steady increase in the number of bookings from 2010 – 2019, with the exception of 2012 – 2013 and 2015 - 2016.
-	There is a fall in the net income from 2013 (261,038.30) to 2014 (180,093.58), even when there is an increase in bookings from 2013 (5525) to 2014 (5905).



### RECOMMENDATION

The steepest increase in net income was observed between 2016 – 2019. Whatever strategy employed during this period for its growth, needs to continue.

### LIMITATION

A data dictionary was not provided.

### REFERENCE

[YouTube](www.youtube.com)

