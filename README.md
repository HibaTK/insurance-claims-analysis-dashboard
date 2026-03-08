# Insurance Claims Analysis Dashboard
## Project Overview
This project analyzes insurance claim data to understand financial exposure, cost drivers, claim denial patterns, and operational efficiency.

Using *Microsoft Power BI*, the dataset was transformed into a dimensional star schema model and an interactive dashboard was built to help stakeholders
monitor claim trends, identify high-cost segments, and detect operational risks in claim processing.

The dashboard focuses on answering key business questions related to:
- Overall financial exposure of claims
- Drivers of claim costs
- Risk segmentation across patient demographics
- Claim approval and denial patterns
- Operational efficiency across submission channels and providers

## Business Questions
The dashboard was designed to answer the following key questions:
- 1 - What is the total financial exposure from insurance claims?
- 2 - Which specialties and procedures drive the highest claim costs?
- 3 - Which demographic segments represent the highest claim risk?
- 4 - Where do claim denials occur most frequently?
- 5 - Which claim submission channels perform most efficiently?
- 6 - Are certain providers or specialties associated with higher operational risk?

## Dataset Description
The dataset contains 4,500 insurance claims with information about patients, providers, diagnoses, procedures, and claim outcomes.

### Key Fields
| Column                | Description                                               |
| --------------------- | --------------------------------------------------------- |
| ClaimID               | Unique identifier for each insurance claim                |
| PatientID             | Unique identifier for each patient                        |
| ProviderID            | Unique identifier for healthcare providers                |
| ClaimAmount           | Dollar value requested for reimbursement                  |
| ClaimDate             | Date the claim was filed                                  |
| DiagnosisCode         | Medical diagnosis identifier                              |
| ProcedureCode         | Medical procedure performed                               |
| PatientAge            | Age of the patient                                        |
| PatientGender         | Gender of the patient                                     |
| PatientIncome         | Income of the patient                             |
| ProviderSpecialty     | Medical specialty of the provider                         |
| ProviderLocation      | Geographic location of provider                           |
| ClaimStatus           | Approved, Denied, or Pending                              |
| ClaimType             | Type of claim (Inpatient, Outpatient, Emergency, Routine) |
| ClaimSubmissionMethod | Submission channel (Online, Paper, Phone)                 |

## Data Model
The dataset was structured using a star schema to improve analytical clarity and scalability.

### Tables
*Fact Table*
- FactClaims
  
*Dimension Tables*
- DimPatient
- DimProvider
- DimDate

Relationships follow one-to-many dimensional modeling principles, allowing efficient filtering and aggregation.

## Key Metrics Created
Several analytical measures were created using DAX:
- Total Claim Amount
- Total Claims
- Average Claim Amount
- Approval Rate
- Denial Rate
- Pending Rate
- Month-over-Month Claim Growth
- Rolling 12-Month Claim Average
- Percentage Contribution to Total Claim Amount

## Dashboard Pages

### *1. Financial Overview*
  
This page provides a high-level summary of claim financial performance.
  
*Key elements include*

- Total claim exposure
- Total number of claims
- Average claim value
- Approval and denial rates
- Monthly financial exposure trends
- Claim distribution by provider specialty
### Insights
- The dataset contains 4.5K claims totaling $22.6M, with an average claim value of approximately $5K.
- Claim outcomes are evenly distributed, with 33.8% approved, 33.6% denied, and the remainder pending review.
- The 12-month rolling average of claim payouts remains stable, indicating consistent financial exposure over time.
- Pediatrics represents the highest cost specialty, contributing $4.8M (21.7%) of total claim value, while other specialties show similar cost contributions.
  
### *2.Cost Drivers & Risk Segmentation*
  
This page identifies where claim costs originate and which demographic segments represent higher financial risk.

*Key analyses include*

- Claim contribution by age group
- Claim contribution by income group
- Cost concentration by diagnosis
- Cost concentration by procedure
### Insights
- Claim costs are widely distributed across procedures and diagnoses, with the top five procedures contributing only 0.36% of total claim value.
- The largest single diagnosis contributes just 0.07% of total claim cost, indicating no single medical condition dominates overall payouts.
- Patients aged 55+ account for 41.1% of total claim value, representing the highest financial exposure.
- The 25–39 age group contributes the lowest claim share (12.3%).
- High-income patients generate 56.4% of total claim value, indicating higher treatment utilization or claim severity within this segment.
- Procedure nR774 ($17.8K) and diagnosis Vy109 ($15.7K) represent the highest individual cost concentrations.

### *3. Denial & Operational Efficiency*
  
This page analyzes claim processing performance and operational efficiency.

*Key analyses include*

- Claim approval and denial distribution
- Denial concentration by claim type
- Approval and denial rates by submission channel
- Provider specialty operational performance
### Insights
- Claim outcomes are evenly distributed across statuses, with approximately 1.5K claims each for approved, denied, and pending categories.
- Outpatient claims account for the highest share of denied claims (25.7%), while emergency claims represent the lowest denial share.
- Phone submissions show the highest approval rate (51.98%), indicating relatively efficient processing through this channel.
- Online submissions exhibit the highest denial rate (52.16%), suggesting potential documentation or validation issues in digital submissions.
- Cardiology appears in the high-volume, high-denial quadrant, indicating potential operational risk requiring closer monitoring.
- General Practice and Neurology show low claim volume but relatively high denial rates, suggesting possible process inefficiencies.
- Orthopedics demonstrates low claim volume and low denial rates, representing a stable operational segment.
   
## Tools Used
- Microsoft Power BI – Data modeling and dashboard development
- DAX – Analytical calculations and KPI creation

## Conclusion
This project demonstrates how insurance claim data can be analyzed to uncover financial exposure trends, cost drivers, and operational inefficiencies.
By combining data modeling, DAX measures, and interactive visualization, the dashboard provides insights that can support better underwriting decisions,
operational improvements, and cost management strategies.
