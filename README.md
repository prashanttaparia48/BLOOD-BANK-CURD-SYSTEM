# BLOOD-BANK-CRUD-AND-INVENTORY-SYSTEM
## Overview
The Blood Bank Inventory & Compatibility Manager is a Python-based command-line application designed to manage blood stock levels efficiently. Beyond simple inventory tracking, the system includes a medical logic engine that automatically determines blood type compatibility. It ensures that when a recipient needs blood, the system suggests only medically safe donor types (e.g., O- for generic usage, specific matches for others) and manages stock deductions accordingly.
The system uses persistent storage (CSV) to ensure inventory data is saved between sessions.

## Features
1. Inventory Management: View real-time stock levels for all 8 standard blood types (A+, A-, B+, B-, AB+, AB-, O+, O-).

2. Smart Compatibility Logic:

3. Automatically identifies valid donors for a specific recipient.

Example: If a recipient needs A+, the system checks inventory for A+, A-, O+, and O-.

4. Donation Tracking: Add new blood units to the inventory with input validation.

5. Safe Dispensing: Prevents dispensing more units than are currently available.

6. Data Persistence: automatically generates and updates a blood_inventory.csv file. If the program is closed, data is saved and reloaded upon the next launch.

7. Input Validation: Ensures only valid blood types and positive integers are entered to prevent data corruption.

## Technologies & Tools Used
# Language: Python 3.x

Libraries:

csv (Built-in): For reading and writing inventory data to the file system.

os (Built-in): For file existence checks.

Interface: Command Line Interface (CLI).

Steps to Install & Run
Prerequisites
You must have Python 3.x installed on your machine.

Installation
Download the file blooddndprgm.py.

Place the file in a folder where you have write permissions (the script needs to create a CSV file in the same directory).

Running the Application
Open your terminal (Command Prompt, PowerShell, or Terminal).

Navigate to the directory containing the script.

Run the following command:

Bash

python blooddndprgm.py
On the first run, the system will automatically create a file named blood_inventory.csv with default stock values.

Instructions for Testing
To ensure the system is working correctly, follow these testing steps:

Test 1: Verify Initial Load

Run the program.

Select Option 1 (Display Current Inventory).

Verify that you see a list of blood types with default values (e.g., O- should have 15 units).

Test 2: Receive a Donation

Select Option 2 (Receive New Units).

Enter Blood Type: O- (Universal Donor).

Enter Units: 5.

The system should confirm the addition. Check Option 1 again to ensure O- is now 20 units (15 + 5).

Test 3: Test Compatibility & Dispensing

Select Option 3 (Dispense Units).

Enter Recipient Blood Type: B+.

The system should list compatible donors: B+, B-, O+, O-.

Select a donor type from the list (e.g., O+).

Enter an amount to dispense (e.g., 2).

The system should confirm the dispense action.

Test 4: Verify Persistence

Select Option 4 to exit the program.

Run the program again (python blooddndprgm.py).

Select Option 1.

Verify that the changes made in Test 2 and Test 3 are still present (The inventory should not have reset to default).
# AUTHOR 
 PRASHANT TAPARIA 
 REG.NO-25BCE11043
 B.TECH IN COMPUTER SCIENCE AND ENGINEERING
 VIT BHOPAL

## output screenshots

 <img width="1470" height="956" alt="Screenshot 2025-11-23 at 3 28 00 PM" src="https://github.com/user-attachments/assets/38cf7919-2dfc-474b-94ed-9fe29458a897" />
<img width="1470" height="956" alt="Screenshot 2025-11-23 at 3 29 36 PM" src="https://github.com/user-attachments/assets/64f33eb4-2ade-42ee-b64d-f7fc92b3c309" />
<img width="1470" height="956" alt="Screenshot 2025-11-23 at 3 31 37 PM" src="https://github.com/user-attachments/assets/15b97481-c9c8-4d3e-85de-cdc845e4f716" />

