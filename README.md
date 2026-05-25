IT Asset Management App
A model-driven Power App for managing IT assets, assignments, and audit logs across departments. Built as a portfolio project to demonstrate Microsoft Power Platform development skills.
Overview
This app allows an IT team to track assets across their lifecycle — from procurement through assignment, repair, and retirement. It uses Microsoft Dataverse as the data layer and includes an automated Power Automate alert when an asset is flagged for repair.
Show Image
Features

Track IT assets by category, status, and asset tag
Assign assets to users and departments
Log asset activity with an audit trail
Automated email alert when an asset status changes to "Under Repair"

Tech Stack

Microsoft Power Apps — Model-driven app
Microsoft Dataverse — Data layer
Power Automate — Automated status change alert

Data Model
IT Asset
ColumnTypeRequiredAsset NameTextYesIT Asset TagTextYesCategoryChoice (Laptop, Monitor, Phone, Peripheral, Other)YesStatusChoice (Available, Assigned, Under Repair, Retired)YesPurchase DateDateNoNotesMultiline TextNo
IT Department
ColumnTypeRequiredNameTextYesLocationTextNo
User
ColumnTypeRequiredNameTextYesEmailTextYesDepartmentLookup → IT DepartmentNo
Asset Assignment
ColumnTypeRequiredIT AssetLookup → IT AssetYesAssigned ToLookup → UserYesAssigned DateDateYesReturned DateDateNo
Audit Log
ColumnTypeRequiredIT AssetLookup → IT AssetYesPerformed ByLookup → UserYesActionChoice (Created, Assigned, Returned, Status Changed, Retired)YesTimestampDate/TimeYesNotesTextNo
Power Automate Flow
Asset Status Change Alert — triggers when an IT Asset record is modified. If the Status field equals "Under Repair", an email notification is sent to the IT administrator.
Show Image
Screenshots
Asset Record
Show Image
Asset Assignments
Show Image
Project Context
This is a portfolio project built to demonstrate Power Platform development skills including model-driven app design, Dataverse data modelling, table relationships, and Power Automate cloud flows. It mirrors the type of IT asset tracking solutions commonly built in enterprise and government environments.
