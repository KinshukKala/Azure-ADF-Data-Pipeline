# Azure Cloud Fundamentals and Data Pipeline Implementation using Azure Data Factory

## Project Overview

This project demonstrates the implementation of a complete data pipeline using **Microsoft Azure** and **Azure Data Factory (ADF)**. The pipeline reads a CSV file stored in **Azure Blob Storage**, validates the file metadata, and copies the file to another location within the Storage Account.

The project provides hands-on experience with Azure cloud services, data integration, and ETL pipeline development.

---

## Objectives

- Understand Azure cloud fundamentals.
- Create and manage Azure resources.
- Configure Azure Blob Storage.
- Build a data pipeline using Azure Data Factory.
- Validate file metadata before processing.
- Copy data from one Blob container to another.
- Execute and monitor the pipeline successfully.

---

## Azure Services Used

- Azure Resource Group
- Azure Storage Account
- Azure Blob Storage
- Azure Data Factory (ADF)
- Azure Identity and Access Management (IAM)

---

## Project Architecture

```text
                 CSV File
                    │
                    ▼
       Blob Storage (raw-data)
                    │
                    ▼
        Azure Data Factory (ADF)
      ┌──────────────────────────┐
      │      Get Metadata        │
      │            │             │
      │            ▼             │
      │        Copy Data         │
      └──────────────────────────┘
                    │
                    ▼
   Blob Storage (processed-data)
```

## Project Workflow

### Step 1: Create Azure Resources

- Created a Resource Group.
- Created an Azure Storage Account.
- Created an Azure Data Factory instance.

### Step 2: Configure Blob Storage

- Created two Blob containers:
  - `raw-data`
  - `processed-data`
- Uploaded a CSV file into the `raw-data` container.

### Step 3: Configure Azure Data Factory

- Created a Linked Service to connect ADF with Azure Blob Storage.
- Created:
  - Source Dataset (`DelimitedText1`)
  - Destination Dataset (`DelimitedText2`)

### Step 4: Build the Pipeline

The pipeline contains two activities:

1. **Get Metadata**
   - Validates:
     - File Exists
     - File Size
     - Last Modified Time

2. **Copy Data**
   - Copies the CSV file from the `raw-data` container to the `processed-data` container.

### Step 5: Execute the Pipeline

- Published the pipeline.
- Executed the pipeline using **Debug**.
- Verified successful execution.

---

## Pipeline Components

### Source

- Azure Blob Storage
- Container: `raw-data`
- File Type: CSV

### Metadata Validation

The **Get Metadata** activity validates:

- File Exists
- File Size
- Last Modified Timestamp

### Data Copy

The **Copy Data** activity copies the CSV file from:

```text
raw-data
```

to

```text
processed-data
```

---

## Expected Output

- Pipeline executed successfully.
- Metadata validated successfully.
- CSV file copied to the destination container.


# Learning Outcomes

- Learned the fundamentals of Microsoft Azure.
- Created and managed Azure cloud resources.
- Configured Azure Blob Storage.
- Built an Azure Data Factory pipeline.
- Connected Azure services using Linked Services.
- Validated file metadata before processing.
- Automated file movement using Copy Data activity.
- Executed and monitored a cloud-based data pipeline successfully.

---

# Technologies Used

- Microsoft Azure
- Azure Blob Storage
- Azure Data Factory (ADF)
- Azure IAM

---

# Author

**Kinshuk Kala**
