# E-Commerce Advertising Platform - Automated Reporting Feature Spec

> **Domain:** SaaS / AdTech / Retail Media
> **Target Product:** E-Commerce Advertising Platform
> **Role:** IT Business Analyst Intern Candidate
> **Author:** Trần Hương Linh


## 1. Business Context & Problem Statement

- **Business Context:** E-commerce sellers (Sellers/Brands) running advertising campaigns on E-commerce platforms need to monitor performance metrics periodically.
- **Problem:** Logging in and exporting reports manually every day is time-consuming and easy to miss important data.
- **Solution:** Design a feature that allows scheduling automated, periodic email delivery of ad performance reports (Spend, Revenue, ROAS/ACoS).


## 2. Requirement Documentation (User Story & Acceptance Criteria)

### User Story

> **As an** E-commerce Advertiser,  
> **I want to** schedule automated email reports for my campaign performance,  
> **So that** I can track my ad metrics regularly without manual data exports.

### Acceptance Criteria (AC)

- **AC 1 (Schedule Config):** Configure sending frequency: `Daily` (08:00 AM daily) or `Weekly` (Every Monday).
- **AC 2 (Report Format):** Attached file format `.CSV` or `.PDF` including fields: Campaign Name, Impressions, Clicks, Spend, Revenue, ACoS/ROAS.
- **AC 3 (Recipients):** Allow configuring a maximum of 3 recipient Emails.
- **AC 4 (Validation):** Display red error text `"Invalid email format"` if an incorrect Email format is entered.


## 3. Flow Diagrams

### User Flow (Interaction Flow & UI Error Handling Modeling)

User Flow clearly represents the main flow (Happy Path), cancellation flow (Cancel Path), and closed-loop validation flow (Validation Flow).

![User Flow](./user-flow.drawio.svg)

### Business Flow (System Business Flow & Automation Modeling)

Business Flow represents how data flows in the Backend, the periodic 08:00 AM Cronjob trigger mechanism, calling E-commerce Ads APIs, and automatically sending report Emails.

![Business Flow](./business-flow.svg)
