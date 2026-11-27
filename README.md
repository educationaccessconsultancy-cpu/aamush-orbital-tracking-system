AAMUSH TECHNOLOGY

ORBITAL INTELLIGENCE

Satellite and Orbital Debris Tracking System

Institutional Project Documentation | Technical Platform Overview

---

1. Institutional Identity

AAMUSH TECHNOLOGY is the institutional technology identity behind the development of the Orbital Intelligence platform.

Orbital Intelligence is a digital platform designed to support satellite catalogue monitoring, orbital object identification, orbital data analysis, satellite tracking and space-debris monitoring.

The platform adopts a data-driven approach to space situational awareness, combining publicly available orbital information, mathematical propagation methods, interactive geospatial visualisation and structured data management.

Its development is guided by the principles of:

- Scientific accuracy and technical integrity.
- Traceable and attributable data sources.
- Transparent orbital information.
- Responsible interpretation of satellite records.
- Reliable data management and preservation.
- Continuous technical development.

2. Project Overview

Orbital Intelligence is intended to provide an integrated environment for examining objects orbiting the Earth.

The platform focuses on three principal categories:

1. Payloads and satellites.
2. Rocket bodies.
3. Orbital debris.

It is designed to transform catalogue information and orbital parameters into interpretable visual and analytical information.

The system distinguishes between an object's catalogue classification, its calculated orbital position and its independently verified operational status.

These are separate technical attributes and must not be treated as interchangeable.

3. Vision and Strategic Objectives

Vision

To develop a reliable, accessible and technically credible orbital intelligence platform supporting the observation, analysis and understanding of artificial objects in Earth's orbital environment.

Strategic objectives

1. Establish a structured satellite and orbital object catalogue.
2. Support the identification of catalogued Earth-orbiting objects.
3. Calculate orbital positions using established propagation methods.
4. Visualise orbital objects in an Earth-centred three-dimensional environment.
5. Distinguish satellites, rocket bodies and debris.
6. Maintain historical and previously validated catalogue records.
7. Support manual orbital data acquisition and import.
8. Improve transparency in orbital data provenance and freshness.
9. Establish a foundation for more advanced space situational awareness capabilities.

4. Core Platform Modules

4.1 Three-Dimensional Earth Visualisation

The platform is designed around an interactive three-dimensional Earth environment.

Intended capabilities include:

- Earth rotation and visual navigation.
- Zoom and viewing-angle control.
- Orbital object visualisation.
- Satellite selection.
- Orbital object identification.
- Inspection of calculated orbital positions.

The visualisation must distinguish illustrative Earth graphics from actual propagated satellite positions.

4.2 Satellite Catalogue Management

The catalogue management module provides a structured environment for storing and examining orbital object records.

Catalogue information may include:

- Object name.
- NORAD catalogue identification number.
- Object classification.
- Orbital inclination.
- Orbital epoch.
- Orbital parameters.
- Calculated orbital altitude.
- Source and data timestamp.

4.3 Space Debris Monitoring

The debris monitoring module is intended to support the identification and classification of orbital debris and rocket bodies.

Its objectives include:

- Distinguishing debris from payload objects.
- Identifying rocket bodies.
- Examining available orbital parameters.
- Visualising classified objects.
- Supporting catalogue-based orbital analysis.

Catalogue classification must not be represented as a complete physical assessment of an object's condition.

4.4 Orbital Propagation Engine

The platform uses the Simplified General Perturbations 4 (SGP4) model for satellite orbital propagation.

The propagation process converts validated orbital element records into calculated positions at specified times.

The intended technical workflow is:

1. Retrieve or import orbital elements.
2. Validate the catalogue records.
3. Parse the orbital parameters.
4. Initialise the SGP4 propagation engine.
5. Calculate object positions.
6. Transform coordinates for visualisation.
7. Display the resulting orbital positions.

The calculated positions depend on the quality, epoch and validity of the underlying orbital elements.

4.5 Object Inspection

The object inspection module is designed to provide detailed information about a selected orbital object.

Users should be able to examine:

- Object identity.
- Catalogue number.
- Object classification.
- Available orbital elements.
- Orbital inclination.
- Calculated altitude.
- Data epoch.
- Source provenance.

The platform must clearly distinguish catalogue-derived information from calculated information.

5. Data Sources and Catalogue Integration

Primary data source

CelesTrak General Perturbations (GP) Data

Official source:

https://celestrak.org/

CelesTrak provides publicly accessible orbital element information for catalogued space objects.

The platform is designed to support modern orbital data formats, including:

- CSV.
- CCSDS Orbit Mean-Elements Message (OMM).

The system should validate incoming records before accepting them into its active catalogue.

Data provenance

Every catalogue update should retain information identifying:

- Original data source.
- Retrieval or import time.
- Data format.
- Catalogue epoch.
- Validation result.
- Connection status.

The system must not present unavailable or unverified information as live orbital data.

6. Resilient Data Management Architecture

Reliable catalogue management is a central technical requirement.

The platform is designed to accommodate temporary network failures and restrictions affecting external data services.

6.1 Controlled Catalogue Retrieval

External catalogue retrieval should follow appropriate request intervals and the data provider's published access policies.

The system should avoid unnecessary repeated requests.

6.2 Persistent Catalogue Caching

Previously validated orbital records should be retained locally using browser-supported persistent storage.

The intended storage architecture includes IndexedDB.

Cached information should retain its original data timestamp and source provenance.

6.3 Manual Catalogue Import

The platform is designed to support manual catalogue acquisition where automated retrieval is unavailable.

Supported import targets include CSV and OMM-compatible records.

Imported records must pass format and data validation before being accepted.

6.4 Failure-Safe Catalogue Updates

The application should never erase a previously validated catalogue merely because a new retrieval attempt fails.

The update process should:

1. Retrieve new catalogue information.
2. Validate the returned records.
3. Check the integrity of the new dataset.
4. Preserve the existing validated catalogue.
5. Replace or update records only after successful validation.
6. Report failures transparently.

An HTTP 403 response must not disable access to locally cached or manually imported orbital records.

7. Data Integrity and Operational Status

Orbital Intelligence recognises an important distinction between orbital information and operational intelligence.

Public orbital elements can support the calculation of an object's position and examination of its orbital parameters.

However, they do not independently establish whether an object is:

- Operational.
- Healthy.
- Controlled.
- Transmitting.
- Actively performing its mission.

Operational status must only be reported when supported by an appropriate authoritative source.

The platform therefore treats operational status as a separate verification category.

8. Technical Architecture

The intended technical architecture comprises the following components:

Component| Technology or standard
Application interface| HTML5
Presentation| CSS3
Application logic| JavaScript
Earth visualisation| Three.js
Orbital propagation| SGP4
Propagation library| satellite.js
Orbital catalogue| CelesTrak GP
Data formats| CSV / CCSDS OMM
Persistent browser storage| IndexedDB
Hosting| GitHub Pages
Version control| Git / GitHub

Actual component availability and successful operation must be verified in the deployed application.

9. Data Security and Scientific Integrity

The platform adopts the following operational principles:

- No fabricated satellite records.
- No invented orbital positions.
- No unsupported operational-status claims.
- Clear identification of unavailable data.
- Preservation of validated catalogue records.
- Transparent reporting of data age.
- Validation of imported orbital elements.
- Attribution of external data sources.

Orbital Intelligence is intended as an orbital information and visualisation platform, not a certified collision-avoidance or conjunction-assessment service.

10. Deployment and Hosting

The platform is hosted through GitHub Pages.

Repository:

https://github.com/educationaccessconsultancy-cpu/aamush-orbital-tracking-system

Public application:

https://educationaccessconsultancy-cpu.github.io/aamush-orbital-tracking-system/

The deployment environment uses the main branch as its publishing source.

Changes to the application should be committed to the repository and verified after deployment.

11. Development Roadmap

The following roadmap establishes the intended direction of continued development.

Phase I — Platform Stabilisation

- Correct application initialisation.
- Establish reliable satellite catalogue retrieval.
- Implement persistent catalogue caching.
- Enable manual CSV and OMM imports.
- Validate orbital element records.
- Restore interactive controls.

Phase II — Orbital Intelligence

- Implement reliable SGP4 propagation.
- Improve satellite and debris classification.
- Develop object inspection.
- Improve orbital visualisation.
- Introduce historical catalogue comparison.

Phase III — Advanced Monitoring

- Develop more detailed orbital analysis.
- Introduce additional authoritative data sources.
- Improve catalogue change detection.
- Develop advanced object classification.
- Expand analytical reporting.

Phase IV — Institutional Development

- Develop structured technical documentation.
- Establish data quality and verification procedures.
- Introduce formal system testing.
- Develop user and administrator documentation.
- Establish a sustainable platform maintenance framework.

These phases describe planned development, not a declaration that all capabilities are currently operational.

12. Technical Limitations

The accuracy and availability of orbital information depend on external data sources, the quality of orbital elements, the propagation model and the browser environment.

The platform may encounter:

- External network restrictions.
- HTTP 403 access responses.
- Data format incompatibilities.
- Outdated orbital elements.
- Browser storage limitations.
- External JavaScript library failures.

Where data retrieval fails, the system should preserve validated local records and report the problem clearly.

A blank catalogue must never be represented as evidence that no orbital objects exist.

13. Institutional and Technical Positioning

AAMUSH TECHNOLOGY positions Orbital Intelligence as a developing digital infrastructure initiative within the broader field of satellite monitoring, orbital data analysis and space situational awareness.

The platform's long-term direction is to provide a structured, transparent and technically responsible environment for examining Earth's orbital population.

Its value is founded on the quality of its data, reliability of its calculations, transparency of its limitations and integrity of its technical implementation.

---

AAMUSH TECHNOLOGY

ORBITAL INTELLIGENCE

Satellite and Orbital Debris Tracking System

Public orbital information. Scientific analysis. Responsible space intelligence.

© 2026 AAMUSH TECHNOLOGY. All rights reserved.