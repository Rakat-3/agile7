http://localhost:8000/api/contracts/active


Project Review Request: Automated Contract Management System
Dear Professor,

I would like to submit the Automated Contract Management System for your review. This project implements a full-lifecycle contract management tool, integrating a modern React frontend with a FastAPI backend and the Camunda BPMN engine to orchestrate complex business workflows.

Technical Architecture
Workflow Engine: Camunda Platform 7 (BPMN 2.0) for process orchestration and role-based task management.
Frontend: React with a glassmorphism design system, featuring dynamic data tables and real-time form validation.
Backend: FastAPI (Python) serving as a robust middleware and providing RESTful APIs for database and process interaction.
Database: Azure SQL Database for persistent storage of contracts and provider offers.
Infrastructure: Fully containerized using Docker and Docker Compose for seamless environment replication.
Key Features Implemented
Unified Contract Lifecycle:
Initiation: A custom "Initialize Contract" interface that triggers the BPMN process directly from the portal.
Review & Approval: Integrated Camunda Tasklist forms with explicit selection mechanisms (radio buttons) for choosing provider offers.
Provider Portal:
A table-based dashboard showing contract IDs, titles, types, and statuses.
Conditional "Make Offer" logic that enforces submission deadlines.
Data Persistence & Sync:
Automatic synchronization between Camunda process variables and the Azure SQL database via dedicated Python external task workers.
Custom API endpoints (e.g., /api/contracts/active) providing real-time JSON exports of finalized contracts.
Security & Robustness:
Fuzzy ID matching and normalization to ensure data integrity across the distributed system.
Refined SQL schemas supporting multiple offers per contract.
Workflow Logic
The system follows a strict BPMN flow: PM Initiation → Provider Tendering → PM Offer Selection → Legal Review → CA Final Storage.

Attached are screenshots of the Contract Dashboard, the Initiation Modal, and the Camunda BPMN Diagram for your reference. I look forward to your feedback.

Best regards, [Your Name]

Suggested Screenshots to include:
Main Dashboard: Showing the list of contracts in the new table view.
Initialize Modal: Showing the form used to start a new contract.
Condition Logic: A shot of the "View Details" modal showing where the "Make Offer" button appears.
Camunda Form: A shot of the 
reviewOffers.form
 in the Camunda Tasklist showing the radio button selection.
