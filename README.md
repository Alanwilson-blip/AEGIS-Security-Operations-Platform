# AEGIS — Security Operations Platform

**A Python-Based Security Monitoring, Threat Detection, and Incident Investigation System**

## 1. Project Overview

AEGIS is a Security Operations Platform developed to organize security activity, detect potentially suspicious access patterns, manage security alerts and incidents, and support structured investigations.

The platform uses Python and Flask for application logic and Microsoft SQL Server for data storage. Its architecture includes authentication, role-based access control, security event processing, risk scoring, incident investigation, audit traceability, and controlled archive and restore workflows.

## 2. Project Objectives

- Process and organize security activity and access events.
- Identify suspicious activity through detection rules.
- Aggregate detection results into risk scores and severity classifications.
- Support security alert and incident management.
- Maintain relationships between incidents, alerts, events, and investigation records.
- Apply authentication and role-based authorization.
- Support audit traceability and controlled data retention.
- Provide archive preview and restore workflows with validation controls.

## 3. Key Features

- **Authentication and Access Control:** Login, session management, CSRF protection, multi-factor authentication, and role-based access control.
- **Threat Detection:** Detection rules D01–D14 and risk-based severity classification.
- **Security Alert Management:** Structured handling of detected security activity.
- **Incident Management:** Organization and tracking of security incidents.
- **Investigation Management:** Investigation records and associated security context.
- **Audit Traceability:** Records supporting accountability for security-related operations.
- **Transactional Archiving:** Archive previews, eligibility checks, relationship validation, and transaction-controlled archival.
- **Restore Workflow:** Preview-first restoration with authorization and validation controls.

## 4. Technology Stack

| Technology | Purpose |
|---|---|
| Python | Backend application logic |
| Flask | Web application framework |
| Microsoft SQL Server | Relational database |
| pyodbc | Python-to-SQL Server connectivity |
| HTML, CSS, JavaScript | Web interface |
| TOTP-based MFA | One-time verification codes |

## 5. Repository Structure

```text
AEGIS-Security-Operations-Platform/
├── app.py
├── auth.py
├── database.py
├── database_queries.py
├── detection_engine.py
├── archive_transaction.py
├── archive_restore.py
├── templates/
├── static/
├── sql/
│   ├── 01_AEGIS_Database_Schema.sql
│   ├── 02_AEGIS_Departments_Roles.sql
│   ├── 03_AEGIS_Resources.sql
│   ├── 04_AEGIS_Permissions.sql
│   ├── 05_AEGIS_Users.sql
│   ├── 06_AEGIS_Devices.sql
│   ├── 07_AEGIS_Access_Events.sql
│   ├── 08_AEGIS_Security_Alerts.sql
│   ├── 10_AEGIS_Test_Scenarios.sql
│   └── 11_AEGIS_Analysis_Queries.sql
├── requirements.txt
├── .env.example
├── .gitignore
└── README.md
```

*Note: This is an illustrative structure. Adjust the filenames and folders to match the actual files included in the repository.*

## 6. Prerequisites

Before setting up the application, ensure that the following are available:

- Python installed on the system.
- Microsoft SQL Server.
- An appropriate SQL Server ODBC driver.
- A database account or Windows authentication configuration with the required permissions.
- The Python dependencies listed in `requirements.txt`.

## 7. Setup and Configuration

1. Clone the repository:

   ```bash
   git clone YOUR_GITHUB_REPOSITORY_URL
   cd AEGIS-Security-Operations-Platform
   ```

2. Create and activate a Python virtual environment:

   ```bash
   python -m venv .venv
   ```

   Windows PowerShell:

   ```powershell
   .\.venv\Scripts\Activate.ps1
   ```

3. Install the project dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Configure Microsoft SQL Server connectivity using the project's configuration files and your local environment.

5. Review the SQL scripts in the `sql/` directory. Execute the appropriate setup scripts in the documented order against a development database, after reviewing their effects.

6. Configure the required environment variables and application secrets. Use `.env.example` as a template if provided; never commit real credentials.

7. Start the application using the project's actual entry-point command.

*Setup commands and configuration must be verified against the committed source files before the project is presented as ready to run.*

## 8. Database Scripts

The SQL scripts are provided to define database objects, configure supporting records, and prepare example security data and analysis queries.

Review each script before execution. Some scripts insert records, modify permissions, or create test scenarios. Use a development database and back up any existing data before running scripts that modify it.

## 9. Security Considerations

- Never commit passwords, API keys, session secrets, MFA secrets, or database credentials.
- Do not publish real user records, confidential incident data, or sensitive security logs.
- Use `.gitignore` to exclude `.env`, virtual environments, cache files, and local database artifacts.
- Review SQL scripts before execution, especially those that reset permissions or modify existing records.
- Keep archive and restore operations restricted to appropriately authorized users.

## 10. Project Documentation

The accompanying project documentation describes the AEGIS architecture, authentication and access control, security event processing, threat detection, incident investigation, database organization, and archive and restore workflows.

## 11. Disclaimer

AEGIS is intended for educational, development, and authorized security operations use. Test the system in a controlled environment before connecting it to operational data or infrastructure.

## 12. Author

**Project:** AEGIS — Security Operations Platform  
**Category:** Cybersecurity / Security Operations  
**Technologies:** Python, Flask, Microsoft SQL Server

