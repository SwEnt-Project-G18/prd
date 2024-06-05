# Design and Implementation

## Frontend

<!---
*List the key libraries, languages, components used by the MVP.*

*If applicable, describe essential screens.*
-->

The app is developed in Kotlin using Jetpack Compose with an MVVM (Model-View-ViewModel) architecture. This setup ensures a modern, responsive UI and a clear separation of concerns, making the app maintainable and scalable.

### Key Libraries and Components

1. **Jetpack Compose:** For building the UI in a declarative manner.
2. **Kotlin Coroutines:** For handling asynchronous operations.
3. **ViewModel:** To manage UI-related data lifecycle-conscious way.
4. **LiveData:** To build data objects that notify views when the underlying database changes.
5. **Retrofit:** For making API calls to the backend.
6. **Firebase Authentication:** For managing user authentication.
7. **Stream Chat SDK:** For integrating real-time chat functionality.
8. **Google Maps Compose:** For displaying events on a map.
9. **Firebase Firestore:** For database management.
10. **QR Code Libraries:** ZXing and JourneyApps for QR code generation and scanning.

### Essential Screens

1. **Home Screen:**
   - Displays the Explore Map with local events.
   - Provides access to the Trends Screen and Recommended Events.

2. **Trends Screen:**
   - Highlights major and trending events.
   - Provides easy access to popular events based on user preferences and interactions.

3. **Event Creation Screen:**
   - Allows users to create new events quickly.
   - Includes options for public or private event settings.

4. **Event Detail Screen:**
   - Shows detailed information about a specific event.
   - Includes options to join, share via QR code, or chat with attendees.

5. **User Profile Screen:**
   - Allows users to view and edit their profile information.
   - Displays user interests and past event participation.

6. **Notification Screen:**
   - Lists all event reminders and updates.
   - Allows users to manage notification settings.

7. **Chat Screen:**
   - Provides real-time messaging capabilities.
   - Supports group chats and direct messages to event organizers.

## Backend

<!---
*Decompose the MVP into functional blocks.*
-->

The backend is designed to support the core functionalities of the app efficiently and securely. The following functional blocks are integral to the backend:

1. **User Management:**
   - Handles user registration, authentication, and profile management.
   - Manages user sessions and access control.

2. **Event Management:**
   - Supports the creation, updating, and deletion of events.
   - Manages event details, RSVPs, and invitations.

3. **Chat System:**
   - Provides real-time chat functionality using Stream Chat SDK.
   - Ensures secure and efficient message handling.

4. **Notification System:**
   - Manages the scheduling and delivery of notifications.
   - Handles reminders for upcoming events and important updates.

5. **Recommendation Engine:**
   - Analyzes user data to provide personalized event recommendations.
   - Continuously improves based on user interactions and feedback.

6. **QR Code Sharing:**
   - Generates QR codes for event sharing.
   - Integrates QR code scanning for easy event joining.

## Data Model

<!---
*What data are you collecting / managing?*

*How is it organized?*

*Where is it stored?*

*How is it shared/copied/cached?*
-->

The two central objects we manage are Users and Events. We will use Firebase as our database system to store and manage this data.

### Data Collection and Management

1. **Users:**
   - User ID, name, email, profile picture, interests, and event history.
   - Authentication tokens and session management data.

2. **Events:**
   - Event ID, title, description, location, date, time, and type (public or private).
   - List of attendees, invitations, and chat messages related to the event.

### Data Organization

- **Users Collection:** Stores all user-related data.
- **Events Collection:** Stores all event-related data.
- **Chats Collection:** Stores chat messages associated with events.

### Data Storage

- **Firebase Firestore:** Used for storing user and event data.
- **Firebase Storage:** Used for storing media files, such as profile pictures and event images.

### Data Sharing and Caching

- **Cloud Functions:** Used for securely sharing and updating data in real-time.
- **Local Caching:** Uses Room database for caching frequently accessed data to improve performance.

## Security Considerations

- **Data Encryption:** Encrypt all sensitive data both at rest and in transit.
- **Access Control:** Implement role-based access control to restrict access to sensitive information.
- **Authentication:** Use Firebase Authentication for secure user login and session management.
- **Regular Audits:** Conduct regular security audits to identify and address vulnerabilities.

## Infrastructure and Deployment

<!---
*How is the application developed, tested and deployed?*

*Any special infrastructure requirements.*
-->

### Development

- **Version Control:** Use Git for version control.
- **CI/CD Pipeline:** Implement continuous integration and continuous deployment pipelines using GitHub Actions.
- **Development Environment:** Use Android Studio for frontend development and Firebase Console for backend management.

### Testing

- **Unit Testing:** Write unit tests for frontend and backend components.
- **Integration Testing:** Perform integration tests to ensure different parts of the system work together correctly.
- **User Testing:** Conduct user testing sessions to gather feedback and identify usability issues.

### Deployment

- **Firebase Hosting:** Deploy the backend services to Firebase.
- **Google Play Store:** Publish the mobile app on the Google Play Store.
- **Monitoring:** Use Firebase Analytics and Crashlytics for monitoring app performance and stability.

## Test Plan

<!---
*How is the application developed, tested and deployed?*

*Any special infrastructure requirements.*
-->

### Testing Strategy

1. **Unit Tests:**
   - Cover core functionalities of the app.
   - Ensure individual components work as expected.

2. **Integration Tests:**
   - Verify the interactions between different modules.
   - Ensure end-to-end functionality.

3. **User Acceptance Testing (UAT):**
   - Conduct testing sessions with actual users from the EPFL community.
   - Gather feedback on usability and functionality.

4. **Performance Testing:**
   - Test the app under various conditions to ensure it can handle peak traffic.
   - Optimize for speed and responsiveness.

### Tools and Frameworks

- **JUnit:** For unit testing the Kotlin codebase.
- **Espresso:** For UI testing of the Android app.
- **Firebase Test Lab:** For running tests on real devices in the cloud.
- **Crashlytics:** For monitoring and tracking crashes in the production environment.

By following this comprehensive design and implementation plan, GoMeet aims to deliver a robust and user-friendly event management app tailored to the needs of college students and event organizers.
