Description: Small (‘next to your home’) beauty salon that provides main basic services: haircuts, manicure, facials, massages. 
This beauty salon has regular and new customers. Regular customers receive 5% discount automatically. New customers get 5%, 10% or 15% discount if they buy 2 or more services, if customer brings flyer or has a birthday, etc. Discounts can be summarized together.  
Application saves following information in csv file ‘appointments’: 
-	Customer’s name 
-	Customer’s telephone number (which is a unique key to check if the customer new/regular)
-	Date of appointment (calendar pops-up)
-	Reminder (if a customer needs to be reminded about coming appointment or not)
-	Services (haircut type, manicure type, facial type, massage type) 
-	Prices for each service
-	Automatically applies discount if any
Application outputs: 
-	Receipt for the customer, that includes: 
a)	customer’s name 
b)	date of appointment
b) services that were provided 
c) discount if any 
d) total price 
e) thank you message 
Application has several ‘stop’ factors: a) if customer’s details are not filled (reminder message appears) b)services are banned until some service is chosen, type of service and price are chosen (appears reminder message as well) c) when admin saves appointment, message ‘appointment is saved’ appears in pop-up window. 
