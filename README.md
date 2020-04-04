BYU/BYUI Ride Board App
=======================

Problem
-------
The [ride board](https://www.facebook.com/groups/536633829764055/) has a lot of active users offering and asking for rides for a very good price.  I use it all the time. The problem is, to find a ride you have to scroll past every post and identify if it suits your needs.  Such needs might be origin, destination, leave date, etc.  This is tedious.

Solution
--------
It would be nice to be able to filter and sort through posts instantly.  This way all you have to do is compare the rides that already suit your needs.


UX
--
Display a feed that lists posts depending on the user filter options.  There are two modes, offering or asking, and each have slightly different options.  Provide a link to the original post on FB to allow the users to message each other and book a ride. **Note**: the app will not handle messaging or booking of rides.  Leave that to FB.

### Filter Options

* offering
  * origin
  * destination
  * leave date
  * return date
  * price for one-way
  * price for two-way
  * no. of seats available

* asking
	* origin
	* destination
	* leave date
	* return date
	* no. of seats to occupy

Authorization
-------------
* the app should be available to anyone that has access to the FB group

Authentication
--------------
* TBD

Prerequisites
----------
* make sure the FB API gives us access to
  1. a private group (assuming an admin is willing to grant us access)
  1. a machine-friendly representation of text with background images
  1. the following post info
    * date posted
    * date updated
    * link to the original post on fb

NLP Parser
----------

### Example Posts
![alt text](https://github.com/baaae/Ride-Board/blob/master/screenshots/Screen%20Shot%202020-04-04%20at%203.59.07%20PM.png "Logo Title Text 1")

1. Determine if offering or asking?
Offering

2. Extract data.
```
  {
    origin: "Salt Lake",
    destination: "Rexburg",
    leaveDate: "Saturday April 04",
    returnDate: null,
    priceOneWay: null,
    priceTwoWay: null,
    seatsAvailable: 3
  }
```

![alt text](https://github.com/baaae/Ride-Board/blob/master/screenshots/Screen%20Shot%202020-04-04%20at%204.01.41%20PM.png "Logo Title Text 1")

1. Determine if offering or asking?
  Asking

2. Extract data.
```
  {
    origin: "Utah",
    destination: "Rexburg",
    leaveDate: "this week",
    returnDate: null,
    seatsNeeded: 2
  }
```
