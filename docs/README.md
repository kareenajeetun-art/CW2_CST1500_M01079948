⸻

🧠 Multi-Domain Intelligence Platform

Course: CST1510 – Coursework 2
Student Name: Kareena Jeetun
Student ID: M01079948
Academic Year: 2024–2025

⸻

roject Overview

This project is a Multi-Domain Intelligence Platform developed incrementally throughout the semester.
It integrates secure authentication, data management, interactive dashboards, and AI-powered assistance into a single cohesive system.

The platform allows authenticated users to:
	•	Analyse cybersecurity incidents
	•	Manage dataset metadata
	•	Track and update IT support tickets
	•	Interact with an AI Assistant to support analysis and decision-making

The application is built using Python, Streamlit, SQLite, and OpenAI API, following good software engineering and security practices.

⸻

🗂️ Project Structure

CW2_CST1510_M01079948/
│
├── app/
│   ├── data/
│   │   ├── db.py
│   │   ├── incidents.py
│   │   ├── datasets.py
│   │   ├── tickets.py
│   │   └── users.py
│   │
│   ├── services/
│   │   └── __init__.py
│   │
│   ├── pages/
│   │   ├── Home.py
│   │   ├── auth.py
│   │   ├── cyber_incidents_dashboard.py
│   │   ├── datasets_metadata.py
│   │   ├── it_tickets.py
│   │   └── AI_Assistant.py
│   │
│   └── __init__.py
│
├── DATA/
│   ├── intelligence_platform.db
│   ├── cyber_incidents.csv
│   ├── datasets_metadata.csv
│   ├── it_tickets.csv
│   └── users.txt
│
├── docs/
│   └── README.md
│
├── .gitignore
├── requirements.txt
└── main.py


⸻

Week 7 – Secure Authentication System

Description

The first stage of the project focused on building a secure authentication system to protect access to the platform.

Key Features
	•	User registration and login
	•	Password hashing using bcrypt
	•	Automatic salt generation
	•	Username validation and duplicate prevention
	•	File-based persistence (users.txt)
	•	Secure logout and session handling

Security Measures
	•	Passwords are never stored in plaintext
	•	One-way hashing ensures credential confidentiality
	•	Input validation prevents weak or invalid credentials

⸻

Database & Data Pipeline (Weeks 8–9)

Database
	•	SQLite database: intelligence_platform.db
	•	Tables created for:
	•	cyber_incidents
	•	datasets_metadata
	•	it_tickets
	•	users

Data Sources
	•	CSV files for initial data population
	•	Database used as the primary persistent storage
	•	CSV ↔ DB integration supported

CRUD Operations

Each domain supports:
	•	Create (insert new records)
	•	Read (load DB / CSV / combined data)
	•	Update (edit tickets and incidents)
	•	Delete (remove incidents or records where applicable)

⸻

Cyber Incidents Dashboard

Features
	•	View incidents from:
	•	Database
	•	CSV
	•	Combined dataset
	•	Automatic schema normalization to avoid crashes
	•	KPIs:
	•	Total incidents
	•	Open incidents
	•	Critical incidents
	•	Filters:
	•	Date range
	•	Severity
	•	Status
	•	Visualizations:
	•	Severity distribution (bar chart)
	•	Incident trends over time (line chart)
	•	Real-time updates when new incidents are added (including AI-inserted incidents)

Technical Highlights
	•	Robust handling of missing or inconsistent columns
	•	Safe normalization prevents KeyError: 'date'
	•	Cached data loading for performance

⸻

Dataset Metadata Dashboard

Features
	•	View and manage dataset metadata
	•	Add new datasets into the database
	•	Display raw and filtered datasets
	•	Metadata includes:
	•	Dataset name
	•	Source
	•	Description
	•	Owner
	•	Creation date

Purpose

This dashboard demonstrates data governance, documentation, and metadata management, which are critical aspects of modern data platforms.

⸻

IT Tickets Dashboard

Features
	•	View tickets from DB, CSV, or combined source
	•	KPIs:
	•	Total tickets
	•	Open tickets
	•	Average resolution time
	•	Advanced filters:
	•	Priority
	•	Status
	•	Assigned technician
	•	Date range
	•	Ticket management:
	•	Insert new tickets
	•	Update ticket status
	•	Visualizations:
	•	Priority vs status (stacked bar chart)
	•	Ticket creation trends
	•	Resolution time histogram

Libraries Used
	•	Altair for enhanced data visualisation
	•	Fallback to Streamlit charts if unavailable

⸻

Week 10 – AI Assistant Integration

Description

An AI Assistant was integrated to support users across all domains.

Capabilities
	•	Answer questions about:
	•	Cybersecurity incidents
	•	Dataset metadata
	•	IT ticket troubleshooting
	•	Chat-style interface
	•	Conversation memory using Streamlit session state
	•	Secure API key handling using secrets.toml

Security
	•	OpenAI API key stored securely
	•	Secrets excluded from GitHub using .gitignore
	•	GitHub secret scanning compliance ensured

⸻

Secrets & GitHub Security

Secrets Management
	•	API keys stored in:

my_app/.streamlit/secrets.toml


	•	This file is never committed

.gitignore

Includes:
	•	Secrets
	•	Databases
	•	Virtual environments
	•	Cache files
	•	Logs

This ensures the repository is safe and compliant with GitHub security rules.

⸻

Testing & Reliability
	•	Tested across:
	•	DB present / DB missing
	•	CSV present / CSV missing
	•	Combined data sources
	•	Graceful fallbacks prevent crashes
	•	Clear error messages for debugging
	•	Cache clearing supported via UI

⸻

Software Architecture
	•	Modular MVC-style structure
	•	Separation of concerns:
	•	Data layer (app/data)
	•	UI pages (app/pages)
	•	Services & helpers
	•	Reusable database helpers
	•	Scalable design for future extensions

⸻

 Conclusion

This project successfully demonstrates:
	•	Secure authentication practices
	•	Robust data pipelines
	•	Interactive dashboards with real-time updates
	•	AI integration within a data platform
	•	Professional software engineering standards

The final system is secure, modular, scalable, and user-friendly, meeting all coursework requirements while reflecting real-world application design.

