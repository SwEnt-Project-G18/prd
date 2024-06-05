# Functional Requirements

<!---
*Max 3 pages.*

*List the key features of the MVP precisely.*

*Include appropriate architectural diagrams.*

*Describe key internal functionality.*
-->

## Discovery

### Explore Map
The core feature of GoMeet is the interactive map that displays local events users can join. This map provides a visual and intuitive way to discover events happening in the vicinity.

- **Map Interface:** The map should be easily navigable with zoom-in and zoom-out capabilities.
- **Event Markers:** Each event will be represented by markers on the map, which users can click to see event details.

### Trends Screen
A dedicated trends screen will highlight major and trending events, making them easily accessible to users.

- **Trending Algorithm:** A continuously improving algorithm will ensure relevant and popular events are displayed.
- **Event Details:** Users can click on events in the trends screen to view detailed information and join.

### Recommended Events
The app will provide personalized event recommendations based on user preferences and behavior.

- **Recommendation Engine:** Uses data from past attendance, followed tags, and friends' activities to suggest events.
- **User Interface:** Recommendations will be presented in a user-friendly interface, potentially in a swipeable format similar to Tinder.

## Event Creation

### Invite Management
Users will be able to send and manage invitations efficiently.

- **Invite Interface:** A simple interface for inviting users to events and tracking RSVP statuses.
- **Notification of Responses:** Organizers will receive notifications about the status of their invitations (accepted, declined, pending).

### Chat
A built-in chat feature will facilitate communication among attendees and organizers.

- **Group Chats:** For smaller events, enabling attendees to communicate with each other.
- **Organizer Chat:** For larger events, allowing attendees to ask questions directly to the organizer.

### Quick Event Creation
The app will enable users to create small events, such as work meetings or social gatherings, with minimal effort.

- **Lean Interface:** A streamlined event creation process requiring just a few clicks.
- **Event Details:** Users can quickly input necessary details like date, time, location, and description.

### QR Code Sharing
Users will be able to share event details quickly and easily using QR codes.

- **Generate QR Codes:** Event organizers can generate QR codes for their events, which can be scanned by attendees to join.
- **QR Code Scanner:** The app will include a built-in QR code scanner to facilitate quick event joining.
- **Shareable Links:** In addition to QR codes, users can share events through links on social media and messaging platforms.

## Time Management

### Notifications
A robust notification system will keep users informed and reminded about their events.

- **Reminder Notifications:** Users will receive reminders at appropriate times to ensure they don’t miss events.
- **Customizable Alerts:** Users can customize notification settings according to their preferences.

### Calendar Integrations
The app will integrate with major digital calendars to sync events seamlessly.

- **Google Calendar Integration:** Allow users to sync events with their Google Calendar.
- **iCloud Calendar Integration:** Support for syncing with iCloud Calendar.
- **Other Calendars:** Potential integrations with other popular calendar services.

## Architectural Diagrams

Below is a high-level architectural diagram illustrating the key components and their interactions within the GoMeet app:

![GoMeet Architectural Diagram](diagram.png)

## Key Internal Functionality

### User Management
Handles user registration, authentication, and profile management. Ensures secure access and personalized experiences.

### Event Management
Supports the creation, editing, and deletion of events. Manages event details, invites, and RSVP statuses.

### Chat System
Powered by Stream API, providing real-time chat capabilities for event attendees and organizers.

### Notification System
Manages the scheduling and delivery of notifications to users, ensuring timely reminders and updates.

### Calendar Integration
Handles synchronization with external calendar services, allowing users to manage their schedules efficiently.

### Recommendation Engine
Analyzes user data to provide personalized event recommendations, enhancing user engagement.

### Trends Algorithm
Processes event data to identify and highlight trending events, ensuring users are aware of popular activities.

### Map Interface
Provides an interactive map for event discovery, enabling users to find events based on their location.

### QR Code Sharing
Facilitates quick and easy sharing of event details using QR codes, enhancing the ease of event participation.

By incorporating these features and functionalities, GoMeet aims to deliver a comprehensive and user-friendly platform for event organization and participation.
