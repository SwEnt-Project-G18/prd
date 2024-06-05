# Non-Functional Requirements

## Security, Privacy, and Data Retention Policies

<!---
*Which are the applicable laws and regulations?*

*What are your internal policies?*

*Which privacy features do you need from the phone?*
-->

### Applicable Laws and Regulations

- **GDPR (General Data Protection Regulation):** Ensuring compliance with European data protection standards.
- **CCPA (California Consumer Privacy Act):** Protecting the privacy rights of users in California.

### Internal Policies

- **Data Minimization:** Only collect and retain necessary user data.
- **User Consent:** Obtain explicit consent from users before collecting sensitive information.
- **Data Encryption:** Encrypt all sensitive data both at rest and in transit to prevent unauthorized access.
- **Access Control:** Implement strict access control measures to ensure that only authorized personnel can access sensitive data.
- **Regular Audits:** Conduct regular security audits to identify and address potential vulnerabilities.

### Privacy Features

- **Location Data:**
  - **Local Processing:** Users' location data will be processed locally on their devices and will not be uploaded to our servers.
  - **Permission Control:** Users can control and revoke location permissions at any time.

- **Chat Content:**
  - **Managed by Stream:** Chat content will be managed by a third-party service (Stream) to ensure secure and efficient message handling.
  - **End-to-End Encryption:** Ensure that chat messages are end-to-end encrypted to maintain privacy.

- **Private Events:**
  - **Privacy Assurance:** Implement measures to ensure that private events remain confidential and are only accessible to invited participants.
  - **Access Control:** Utilize access control mechanisms to prevent unauthorized access to private event details.

## Adoption, Scalability, and Availability

<!---
*What kind of traffic patterns do you expect to see?*

*Are there known periods of bursty traffic that the MVP must be designed to support?*
-->

### Traffic Patterns

- **Steady Growth:** Anticipate a steady increase in user base as the app gains popularity, especially within target communities such as college campuses.
- **Event-Based Spikes:** Expect significant traffic spikes during major events, particularly when new events are announced or ticket sales open.

### Burst Traffic Handling

- **Ticketing System:**
  - Inclusion of a ticketing system can lead to massive connection spikes at the start of ticket sales for large events.
  - Implement scalable infrastructure that can handle sudden bursts of traffic without degrading performance.

### Scalability

- **Elastic Infrastructure:** Utilize cloud services with elastic scalability to dynamically allocate resources based on traffic demand.
- **Load Balancing:** Implement load balancing to distribute traffic evenly across servers and prevent any single point of failure.
- **Caching:** Use caching strategies to reduce server load and improve response times during peak traffic periods.

### Availability

- **High Availability (HA):**
  - Design the system to be highly available with minimal downtime.
  - Use redundancy and failover mechanisms to ensure continuous operation in the event of hardware or software failures.

- **Disaster Recovery:**
  - Develop a robust disaster recovery plan to quickly restore services in case of catastrophic failures.
  - Regularly back up data and test recovery procedures to ensure readiness.

By addressing these non-functional requirements, GoMeet aims to provide a secure, reliable, and scalable platform that meets the needs of both event organizers and attendees while ensuring compliance with applicable laws and regulations.
