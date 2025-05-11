# Backend Features Requirements

## 1. User Authentication
- **API Endpoints:**
  - `POST /api/auth/register`: Registers a new user.
  - `POST /api/auth/login`: Logs in an existing user.
  - `POST /api/auth/logout`: Logs out the current user.
- **Input/Output Specifications:**
  - Input: User email, password.
  - Output: JWT token, user details.
- **Validation Rules:**
  - Password must be at least 8 characters.
  - Email must be valid.

## 2. Property Management
- **API Endpoints:**
  - `POST /api/properties`: Adds a new property listing.
  - `PUT /api/properties/{id}`: Updates an existing property.
  - `DELETE /api/properties/{id}`: Deletes a property listing.
- **Input/Output Specifications:**
  - Input: Property details (title, description, price, location, etc.).
  - Output: Property listing ID and status message.
- **Validation Rules:**
  - All property fields are required.
  - Price must be a positive number.

## 3. Booking System
- **API Endpoints:**
  - `GET /api/bookings`: Fetches all bookings for a user.
  - `POST /api/bookings`: Creates a new booking.
- **Input/Output Specifications:**
  - Input: Property ID, user ID, booking dates.
  - Output: Booking confirmation, booking details.
- **Performance Criteria:**
  - System should respond to booking requests within 2 seconds.
