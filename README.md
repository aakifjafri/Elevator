Probleum Statement: 

Consider we are building an algorithm for an elevator system for a highrise building like Burj Khalifa. Typically these buildings would have a considerable number of floors / stops. E.g. Burj Khalifa has 165 but let us assume that the number can go upto 200. Given the number of lifts are N, M people who are requesting lifts rapidly. Design an algorithm which would solve these problems

Minimise the wait time for each lift.
In the mornings a lot of people would be going to their respective offices [8-9] so in the morning load of people going up would be high
In the evenings a lot of people would be going down so the load will be high but it will be random
Sometimes when a lift arrives it is full. We would like to avoid that situation also.

Solution:

Whenever a passenger presses an elevator button it becomes a request and it is added to requests array. Requests Array contains list of request objects.

Request : {
	id
	floorNumber
	direction -  (up or down)
	time 
	assigned : elevatorNumber
}
There is list of elevators. An Elevator object has following schema.

Elevator {
	elevatorNumber
	state : idle/ up/ down
	fullCapacity : true / false
	floorNumber
	stops : [ ]     (floor numbers in sorted order)
}

Initialize all elevators as below

{
	elevatorNumber = 1, 2, etc.  (unique identifier)
	state = idle
	fullCapacity = false
	floorNumber = 0, 1, etc.
	stops [ ]  - empty array
}


When a request comes, check for the nearest elevator and assign the request to the elevator. The nearest elevator is chosen by checking elevators

* without full capacity
* finding the difference of floors with current passenger floor
* if an elevator is idle or the elevator going in the same direction as the passenger.
* reassign an already assigned elevator if elevator is fully loaded.
Probleum Statement: 

Consider we are building an algorithm for an elevator system for a highrise building like Burj Khalifa. Typically these buildings would have a considerable number of floors / stops. E.g. Burj Khalifa has 165 but let us assume that the number can go upto 200. Given the number of lifts are N, M people who are requesting lifts rapidly. Design an algorithm which would solve these problems

Minimise the wait time for each lift.
In the mornings a lot of people would be going to their respective offices [8-9] so in the morning load of people going up would be high
In the evenings a lot of people would be going down so the load will be high but it will be random
Sometimes when a lift arrives it is full. We would like to avoid that situation also.

Solution:

Whenever a passenger presses an elevator button it becomes a request and it is added to requests array. Requests Array contains list of request objects.

Request : {
	id
	floorNumber
	direction -  (up or down)
	time 
	assigned : elevatorNumber
}
There is list of elevators. An Elevator object has following schema.

Elevator {
	elevatorNumber
	state : idle/ up/ down
	fullCapacity : true / false
	floorNumber
	stops : [ ]     (floor numbers in sorted order)
}

Initialize all elevators as below

{
	elevatorNumber = 1, 2, etc.  (unique identifier)
	state = idle
	fullCapacity = false
	floorNumber = 0, 1, etc.
	stops [ ]  - empty array
}


When a request comes, check for the nearest elevator and assign the request to the elevator. The nearest elevator is chosen by checking elevators

* without full capacity
* finding the difference of floors with current passenger floor
* if an elevator is idle or the elevator going in the same direction as the passenger.
* reassign an already assigned elevator if elevator is fully loaded.
