BYU/BYUI Ride Board App
=======================

Problem
-------
The ride board is very nice to use bc you can always find rides for the low. The problem is that one
has to scroll all the way down for a while just to find what you're looking for.

Solution
--------
It would be nice to have an app that allows the user to filter, sort, and compare rides instantly.


UX
--
Display a feed that lists posts depending on the user filter options.  There are two modes, offering
or asking, and each have slightly different options.  Each representation of the post should display
all of the filter option info if available along with author name, and other nice-to-haves.  There
should also be a link to the original post to allow the user to message and book a ride.
 Note: the app will not handle messaging or booking of rides.  Leave that to FB.

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
  1. a private group (assuming an admin accepts)
  2. the complete feed of the group
  3. a machine-friendly representation of text with background images
  4. the following post info
    * date posted/updated
    * link to the original post on fb

NLP Parser
----------

### Example Posts
![alt text](https://www.dropbox.com/s/ledb9yrjy34s7ln/Screen%20Shot%202020-04-04%20at%204.01.41%20PM.png?dl=0 "Logo Title Text 1")
![alt text](https://www.dropbox.com/s/2cggujcfvc7ipt9/Screen%20Shot%202020-04-04%20at%203.59.07%20PM.png?dl=0 "Logo Title Text 1")
