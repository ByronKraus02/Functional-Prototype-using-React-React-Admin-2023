# Development and Implementation of a Student Accommodation Management System
### Essay: Developing the Student Accommodation Management System for StelStay Properties

#### Introduction

In our SI/ISM 354 course, my team and I developed a functional information system to manage student accommodation for StelStay Properties, a fictional company tasked with building residential communities for students in Stellenbosch. The objective was to create a system that would handle student lease applications and support administrative functionalities, including managing buildings, apartments, and room assignments. This explains how we approached the project, utilizing both system design techniques and the final outcome, referencing the UML activity diagram and the Entity-Relationship Diagram (ERD) created for the project.

#### System Design and Development

**Project Scope and Requirements**

The goal of our system was to streamline the lease application process for students while providing administrators with tools to manage available properties, approve or deny applications, and assign students to rooms. The system also needed to handle information related to bill payers, since students often had someone else paying for their accommodation. We designed the system using React and React-admin for the front end, with a backend of our choice, which facilitated communication between the database and the user interface.

**Entity-Relationship Diagram (ERD)**

To model the data structure, we created an ERD (Entity-Relationship Diagram) that defines the relationships between various entities within the system. The primary entities include **Students**, **Bill Payers**, **Properties**, **Administrators**, and **Lease Applications**. This diagram provides a clear picture of how each entity interacts with the system and what key attributes are associated with them.

- The **Student** entity stores student details such as name, email, phone number, course, and year of study.
- The **Lease Application** entity captures the lease request made by the student, including the year of the lease and information about the property.
- The **Property** entity details each property’s address, unit number, and room number, while the **Room** entity defines specific apartment types and the rooms available.
- The **Bill Payer** entity stores billing information such as account number, full name, and address of the person responsible for the student’s lease.
- The **Administrator** entity defines system admins who manage the process by approving or rejecting lease applications.

The relationships depicted in the ERD were vital in ensuring that the database structure was well-organized, with each entity properly linked. For example, the **Lease Application** links the student to the bill payer, showing that the lease is managed by an administrator and associated with a specific property.

**Activity Diagram for Lease Processing**

We created an activity diagram to represent the lease application workflow. This UML diagram outlines the interactions between users (students) and system administrators during the application process.

1. **Making a Lease Application**: A student submits a lease application, which is logged by the system. The request is then reviewed by an administrator.
   
2. **Application Processing**: Once the lease request is submitted, administrators check for the availability of rooms. If rooms are available, they proceed with further actions; otherwise, the application is denied.
   
3. **Approval or Denial**: If the room is available, the administrator assigns it to the student. The status of the application is updated, and the student is notified whether their lease has been approved or denied.
   
4. **Lease Acceptance**: If approved, the student receives the lease confirmation and room assignment. If denied, they receive a notification, allowing them to explore other options.

This diagram ensured that our system followed a logical and efficient flow for both students and administrators, minimizing potential bottlenecks during the lease approval process.

#### Key Features Implemented

1. **Student Application Management**:
   The core functionality of our system was to allow students to apply for accommodation. The application form captured essential details like the student’s name, ID, program, year of study, and the lease year. These details were then passed to administrators for processing.

2. **Administrative Tools**:
   Administrators could view pending applications, check the availability of rooms, and assign students to specific rooms. This system allowed them to efficiently manage room occupancy and keep track of assigned leases. The status of the application—whether approved or denied—was dynamically updated.

3. **Bill Payer Management**:
   Since many students have their accommodation paid for by a third party (the bill payer), the system incorporated a way to capture the bill payer’s information, including their name, contact details, and bank information. This feature ensured that invoices and communication could be correctly routed to the responsible party.

#### Testing and Presentation

During the testing phase, we focused on ensuring that the system handled both valid and invalid data correctly. For example, when a student applied for accommodation in a fully booked apartment, the system would automatically deny the request and notify the student. Conversely, if space was available, the system would assign the student to a room and generate a confirmation.

The presentation of our project highlighted the lease application process from both the student and admin perspectives. Demonstration data helped showcase how the system worked in real-time, allowing the evaluators to see how applications were processed, approved, or rejected based on room availability.

#### Challenges and Lessons Learned

One of the main challenges we encountered was designing a backend that could efficiently handle lease requests and room assignments while maintaining data integrity. To solve this, we focused on refining our ERD, ensuring that the relationships between entities were clear and that each application could be linked correctly to a property and a bill payer.

Additionally, building a seamless interface with React-admin required careful planning to ensure that admins could manage tasks like approving leases and assigning rooms without technical difficulties. We learned the importance of breaking down complex tasks into manageable components, ensuring that each feature was well-tested before integration.

#### Conclusion

This project provided an in-depth experience in designing and implementing an information system for managing student accommodation. By using well-structured diagrams, including the ERD and the activity diagram, we were able to create a clear blueprint for the system. Our final prototype successfully handled the core functionalities of lease applications, room assignments, and administrative management, meeting the project’s requirements and providing a functional solution for StelStay Properties.
