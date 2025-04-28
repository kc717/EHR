<h1 align="center">OpenMRS Oral Health Risk Assessment for Burn Patients</h1>

<p align="center"><i>Standardized clinical tool to assess oral health risks in burn injury patients integrated with OpenMRS</i></p>

---

## Project Overview

The **OpenMRS Oral Health Risk Assessment for Burn Patients** is a web-based application designed to enable healthcare providers to systematically evaluate oral health risks in patients with facial burn injuries. 

The tool integrates with the OpenMRS backend, collects clinical, dental, and psychosocial data, calculates a composite risk score, and saves assessment results directly into the electronic health record (EHR).

---

## Features

- **Patient Search**: Retrieve patient data from OpenMRS using a unique identifier.
- **Structured Assessment Form**: Capture data on burn injuries, oral health indicators (DMFT, CPI, OHI, OHIP scores), and psychosocial factors.
- **Automated Risk Calculation**: Calculate composite risk scores and categorize patients as Low, Moderate, or High risk.
- **Encounter Saving**: Save assessment results into OpenMRS with standardized UUID mappings.
- **Assessment History**: View previous oral health assessments for each patient.
- **SNOMED CT Search**: Integrated real-time search for SNOMED CT clinical concepts.

---

## System Architecture

- **Frontend**: HTML5, CSS3, JavaScript (jQuery)
- **Backend**: OpenMRS REST API (Basic Authentication)
- **Terminology Services**: SNOMED CT Snowstorm API
- **Deployment**: Client-side web application

---

## Workflow Overview

1. **Patient Lookup**: Search for patients by identifier through OpenMRS REST API.
2. **Data Entry**: Complete the assessment form with clinical and psychosocial details.
3. **Risk Calculation**: Compute a weighted composite score automatically.
4. **Result Saving**: Save assessment data as an encounter in OpenMRS.
5. **Review History**: Retrieve and display prior assessments.

---

## Installation and Setup

### Prerequisites

- Access to an OpenMRS instance with REST API enabled.
- API credentials (username and password).
- Configured concept UUIDs for each assessment field in OpenMRS.

### Local Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/Subinaghimir/EHR-GROUP.git
   cd EHR-GROUP
Open the index.html file directly in a web browser, or use a local development server:

    python3 -m http.server 8000

    Access the application at http://localhost:8000.

    Update configuration variables inside the JavaScript if necessary:

        API base URL

        Authorization credentials

        Encounter Type UUID and Concept UUIDs

Configuration Notes

    Encounter Type UUID: Required for associating assessments within OpenMRS.

    Concept UUIDs: All data fields must be mapped to corresponding concepts in OpenMRS.

    Authentication: Basic authentication is used; secure credential handling is recommended for production.

    SNOMED CT Search: Powered via Snowstorm API for standardized clinical terminology.

Clinical Rationale

Burn patients, particularly those with facial injuries, experience elevated oral health risks due to functional impairments, psychosocial stressors, and changes in hygiene behaviors.

Early identification and management of oral health risks through structured assessments improve preventive care outcomes and enhance long-term patient quality of life.
Future Enhancements

    Role-based access controls.

    Machine learning-driven dynamic risk prediction models.

    Auto-population of certain fields from existing OpenMRS data.

    Secure token-based authentication.

    Multilingual and accessibility support.
