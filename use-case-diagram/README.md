# Use Case Diagram - Airbnb Clone Backend

## Overview
This directory contains the use case diagram for the Airbnb Clone backend system, which visualizes the interactions between different actors (users) and the system functionalities. The diagram illustrates how guests, hosts, admins, and automated systems interact with various features of the platform.

## Files in this Directory
- `airbnb-usecase-diagram.png` - Visual representation of the use case diagram
- `airbnb-usecase-diagram.plantuml` - PlantUML source code for the diagram
- `README.md` - This documentation file

## Diagram Description

### Actors
The system includes the following key actors:

#### Primary Actors
- **Guest** 👤 - End users who search for and book properties
- **Host** 🏠 - Property owners who list and manage their properties
- **Admin** 👨‍💼 - System administrators who manage the platform

#### Secondary Actors
- **System** 🔧 - Automated system processes and background tasks
- **Payment Gateway** 💳 - External payment processing service
- **Email Service** 📧 - External email notification service

### Use Case Categories

#### 1. User Management
Core functionality for user account operations:
- **Register** - Create new user accounts
- **Login/Logout** - Authenticate users and manage sessions
- **Update Profile** - Modify user profile information
- **Reset Password** - Password recovery functionality

#### 2. Property & Search
Property listing and discovery features:
- **Browse Properties** - View available property listings
- **Search Properties** - Find properties using filters and criteria
- **View Details** - Access detailed property information
- **Create Listing** - Add new property listings (Host only)
- **Edit Listing** - Modify existing property information (Host only)
- **Delete Listing** - Remove property listings (Host only)
- **Upload Photos** - Add property images (Host only)
- **Set Availability** - Manage property availability calendar (Host only)
- **Set Pricing** - Configure property pricing (Host only)

#### 3. Booking & Payment
Reservation and financial transaction management:
- **Make Booking** - Create property reservations
- **Cancel Booking** - Cancel existing reservations
- **Make Payment** - Process payment transactions
- **Manage Bookings** - Oversee booking operations (Host only)
- **Approve Bookings** - Accept or decline booking requests (Host only)
- **Receive Payments** - Host payment processing (Host only)
- **View History** - Access booking history
- **View Earnings** - Monitor financial earnings (Host only)

#### 4. Communication
Messaging and review functionality:
- **Send Messages** - Inter-user communication
- **Leave Review** - Submit property reviews and ratings
- **Respond to Reviews** - Reply to guest reviews (Host only)
- **Communicate with Guests** - Direct host-guest messaging (Host only)

#### 5. Admin & System
Administrative and automated system functions:
- **Manage Users** - User account administration (Admin only)
- **Moderate Content** - Review and approve content (Admin only)
- **Handle Disputes** - Resolve user conflicts (Admin only)
- **Generate Reports** - Create system reports (Admin only)
- **Monitor System** - System health monitoring (Admin only)
- **View Analytics** - Access platform analytics (Admin only)
- **Process Payments** - Automated payment processing (System)
- **Send Notifications** - Automated notification delivery (System)
- **Update Availability** - Automatic availability updates (System)
- **Calculate Fees** - Automated fee calculations (System)
- **Validate Data** - Data integrity checks (System)

## Key Relationships

### Include Relationships
These represent mandatory dependencies between use cases:
- **Make Booking** includes **Make Payment** - Bookings require payment processing
- **Make Booking** includes **Update Availability** - Bookings update property availability
- **Make Payment** includes **Calculate Fees** - Payments require fee calculations
- **Create Listing** includes **Upload Photos** - Property listings require images
- **Approve Bookings** includes **Send Notifications** - Approvals trigger notifications

### Extend Relationships
These represent optional extensions to base use cases:
- **Reset Password** extends **Login/Logout** - Password reset is an optional login feature
- **Cancel Booking** extends **Make Booking** - Cancellation is an optional booking action

## Actor Inheritance
- **Host** inherits all **Guest** capabilities, meaning hosts can also book properties as guests
- This reflects the real-world scenario where property owners may also travel and book accommodations

## External System Dependencies
- **Payment Gateway** - Required for secure payment processing
- **Email Service** - Required for sending notifications and communications

## Business Rules Represented
1. **Authentication Required** - Most use cases require user authentication
2. **Role-based Access** - Different actors have access to different functionalities
3. **Payment Integration** - All booking transactions must include payment processing
4. **Automated Notifications** - System automatically sends notifications for key events
5. **Content Moderation** - Admin oversight for user-generated content

## System Boundaries
The diagram clearly shows the system boundary by distinguishing between:
- **Internal Use Cases** - Functionality provided by the Airbnb Clone system
- **External Actors** - Third-party services that the system depends on
- **User Interactions** - Direct user actions on the platform

## Usage Notes
- This diagram serves as a high-level overview of system functionality
- Each use case represents a complete user goal or system function
- The diagram helps identify required API endpoints and system components
- Use cases will be converted to user stories for development planning

## Next Steps
1. Convert use cases to detailed user stories
2. Define acceptance criteria for each use case
3. Prioritize use cases for development phases
4. Map use cases to specific API endpoints
5. Create detailed sequence diagrams for complex use cases

---

*This use case diagram provides the foundation for understanding the scope and interactions within the Airbnb Clone backend system.*