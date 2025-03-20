# SECURE-CODE
Secure Code Hackathon - Segregation of Duties (SoD) Analyzer

1. Project Overview

This project is a deterministic, high-performance C++ solution designed for financial access risk analysis in ERP systems. The goal is to identify Segregation of Duties (SoD) conflicts, ensuring that no single user can perform conflicting actions (e.g., "Create Payables Invoices" and "Approve Payables Invoices").

This solution processes user-role mappings, privilege assignments, and SoD rules using optimized role-based access control (RBAC) logic and high-performance data structures. The implementation is fully Dockerized, allowing seamless execution with no modifications required by the evaluator.

2. Features

Deterministic Algorithm: Produces the same output for the same input, ensuring consistency.

Optimized RBAC Engine: Efficiently expands role hierarchies and privilege mappings.

Fast Conflict Detection: Uses hash-based lookup tables to speed up SoD violation detection.

Dockerized Execution: The solution is containerized to ensure portability across environments.

3. Setup and Execution Instructions

3.1 Prerequisites

Docker (Install from Docker Official Site)

Excel Data Files (Provided by the competition organizers)

3.2 Building the Docker Image

Run the following command in the project root directory:

3.3 Running the Container with Input Data

Execute the program by mounting the test dataset:

3.4 Expected Output

The tool generates a CSV file (results.csv********************) listing all SoD conflicts with the following columns:

SoD Rule Name

User Name

Role (Leg 1)

Access Point (Leg 1)

Conflicting Role (Leg 2)

Type of Conflict

Create & Approve Payables

John Doe

Accounts Payable Specialist

Approve Payables

Payment Approval Duty

High Risk

3.5 Cleanup (Optional)

To remove the Docker container after execution:

4. Dependencies

All dependencies are pre-installed in the Docker container, ensuring a smooth execution without additional setup.

Operating System: Ubuntu 22.04 (inside Docker)

C++ Compiler: g++

Excel File Handling: xlsxio

Standard Libraries: C++ STL (unordered_map, unordered_set, vector, thread, mutex)

5. Repository Structure

6. Notes for Evaluators

The Dockerized solution is self-contained, meaning evaluators do not need to modify the source code.

The algorithm strictly follows deterministic principles, ensuring accuracy and reproducibility.

The output format strictly adheres to the competition requirements.

The repository does NOT include test data due to competition rules.

For any questions, refer to the provided documentation or contact the project author.

7. Additional Resources

Docker Official Documentation

C++ Multithreading (std::thread)

Segregation of Duties (SoD) Concept



ROHAN JAIN,DEBDEEP BANERJEE (TEAM DR)

March 2025

