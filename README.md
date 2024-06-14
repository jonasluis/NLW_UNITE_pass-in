This project is an API built using Java, Java Spring, Flyway Migrations, HSQLDB as the database.

This project simulates the operation of an in-person event management dashboard, built during Next Level Week Unite, a free event where I built the project from scratch to teach the community of developers starting in the area.

Table of Contents
Requirements
Installation
Configuration
Usage
API Endpoints
Requirements
Functional requirements
 The organizer must be able to register a new event.
 The organizer must be able to view event data.
 The organizer must be able to view the list of participants.
 The participant must be able to register for an event.
 The participant must be able to view their registration badge.
 The participant must be able to check-in at the event.
Business rules
 Participants can only register for an event once.
 Participants can only register for events with available places.
 Participants can only check-in to an event once.
Non-functional requirements
 Check-in at the event will be carried out using a QRCode.

 Usage
Start the application with Maven
The API will be accessible at http://localhost:8080
API Endpoints
The API provides the following endpoints:

POST /events - Register a new event.

GET /events/{eventId} - Retrieve event details.

GET /events/attendees/{eventId} - Retrieve the list of participants registered for specified event.

POST /events/{eventId}/attendees - Register a new participant to event.

POST /attendees/{attendeeId}/badge - Retrieves participant badge to access the event.

POST /attendees/{attendeeId}/check-in - Check in participant in the event.
