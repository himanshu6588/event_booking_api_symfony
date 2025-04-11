# Event Booking API

A RESTful API for an Event Booking System built with Symfony.

## Features

- Event Management: Create, update, delete, and list events
- Attendee Management: Register and manage attendee information
- Booking System: Book events with validation for overbooking and duplicate bookings
- Pagination and filtering for listing events
- Docker support for easy deployment

## Requirements

- PHP 8.1 or higher
- Composer
- Docker and Docker Compose (for containerized setup)
- MySQL 8.0

## Installation

### Using Docker

1. Clone the repository:
```bash
git clone <repository-url>
cd event-booking-api

## API Documentation
### Events
- GET /api/events - List all events (with pagination and filtering)
- GET /api/events/{id} - Get a specific event
- POST /api/events - Create a new event
- PUT /api/events/{id} - Update an existing event
- DELETE /api/events/{id} - Delete an event
### Attendees
- GET /api/attendees - List all attendees
- GET /api/attendees/{id} - Get a specific attendee
- POST /api/attendees - Create a new attendee
- PUT /api/attendees/{id} - Update an existing attendee
- DELETE /api/attendees/{id} - Delete an attendee
### Bookings
- GET /api/bookings - List all bookings
- GET /api/bookings/{id} - Get a specific booking
- POST /api/bookings - Create a new booking
- DELETE /api/bookings/{id} - Cancel a booking


## Running the Event Booking API

##To run the project in your browser, you'll need to start the Docker containers first. After starting the containers, the application will be accessible at:

URL : http://localhost:8080

## When you access this URL, the first file that gets called is public/index.php . This is the front controller for Symfony applications and serves as the entry point for all web requests.

## To start the project:

1. Make sure Docker and Docker Compose are installed on your system
2. Navigate to the project directory in your terminal
3. Run the following command:
```bash
docker-compose up -d
 ```

4. Create the database schema:
```bash
docker-compose exec php bin/console doctrine:schema:create
 ```
```

5. (Optional) Load the sample data:
```bash
docker-compose exec php bin/console doctrine:fixtures:load
 ```
```

## Once these steps are completed, you can access the API at http://localhost:8080 and the API documentation at http://localhost:8080/api/docs .
