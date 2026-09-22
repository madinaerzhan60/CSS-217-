**Library Room Booking system:**
-

This system has :
* Users (Students, Admin, Staff)
* Rooms (List of Available rooms)
* Bookings (Logic to reserve room)


**Organizational Topology**
-
- maybe small internal IT department at SDU 

**Domain complexity**
- 
- Complexity level -  low to medium.

-  The only hard part is handling many requests at the same time during midterm or exam weeks. The rest of the app is just basic data saving.


**Team maturity**
-
Experience: The developers know how to build standard web applications and use simple SQL databases

**Architecture options**
-

**Option A: Microservices**

What it is: Splitting the system into 3 separate apps (Users app, Rooms app, Bookings app) that talk over the network.

Pros: If one app breaks, the others can still work.

Cons: Too difficult to build and connect for a small IT department.

**Option B: Modular Monolith**

What it is: One single application and one database. But the code is cleanly separated into folders (Modules) for Users, Rooms, and Bookings.

Pros: Easy to build, fast to deploy, and simple to stop double-bookings in one database.

Cons: If the main server crashes, the whole system stops working.


**The best choice is a Modular Monolith.**
-
Why? Good for the Team - A small IT department at SDU can build and fix one single codebase much faster.

The project complexity is low, so we do not need a complicated distributed system.

 I choose fast development. The bad side is a single point of failure (if the server dies, the app dies). This is okay for a university library.
 
  One database makes it very easy to lock room times and prevent double-bookings without complex network rules.



