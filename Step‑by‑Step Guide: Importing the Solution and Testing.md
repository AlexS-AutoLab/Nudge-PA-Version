
Power Automate Nudge App
Step‑by‑Step Guide: 
Importing the Solution and Testing
This document explains how to import the Power Automate Nudge App solution into your own Power Platform environment, configure the required settings, and perform basic testing.

⚠️ Important
This solution is provided for development and learning purposes only.
It is not a fully supported or production‑ready deployment.


1. Prerequisites
Before you begin, ensure the following are in place:

Access to a Power Platform environment (Development or Sandbox recommended)
Permission to import solutions
Access to a SharePoint site where files can be stored
A Microsoft 365 group containing Copilot‑enabled users (for targeted nudges)


2. Upload the JSON Adaptive Card to SharePoint
The Nudge App uses a JSON file that defines the Adaptive Card. This file must be uploaded to a SharePoint document library before importing the solution.
Steps

Go to your SharePoint site
Navigate to (or create) a document library
Example: Nudge App Adaptive Cards
Upload the JSON Adaptive Card file(s) into this library
Confirm:

<img width="996" height="460" alt="Screenshot 2026-01-19 143124" src="https://github.com/user-attachments/assets/3669ac03-1659-4d43-8616-649230c3fe24" />


The file is visible
The file name matches what you expect to reference
You have access to the library



✅ At the end of this step, the JSON file should be stored and accessible in SharePoint.

3. Import the Solution into Power Platform
Once the JSON file is available in SharePoint, you can import the solution.
Steps

Go to Power Apps → Solutions
Select Import
Upload the solution package (.zip)
Proceed with the import wizard


4. Configure Connection References
During the import process, Power Platform will prompt you to re‑establish connections.
Typical connectors used in this solution include:

SharePoint
Office 365 Groups
Microsoft Teams

What to do

Sign in when prompted
Ensure each connection shows a green check mark
This ensures all flows and integrations can run correctly
<img width="661" height="408" alt="Screenshot 2026-01-19 143312" src="https://github.com/user-attachments/assets/79b21479-2465-43f3-983c-3096d2a16e37" />


✅ Do not continue until all required connections are resolved.

5. Set Environment Variable Values
While importing the solution, you will be asked to populate environment variables. These values are mandatory for the solution to function.
Required configuration details
1. Site Address

The URL of the SharePoint site where the Adaptive Card JSON file is stored
Example:
https://contoso.sharepoint.com/sites/M365Copilot



2. Library Name

The name of the SharePoint document library containing the JSON file
Example:
Nudge App Adaptive Cards



3. Group ID

The Microsoft 365 Group ID that contains all Copilot‑enabled users
This group is used for targeted communication and nudging actions
<img width="687" height="442" alt="Screenshot 2026-01-19 143359" src="https://github.com/user-attachments/assets/4590987f-abb4-4795-92d1-20713767e930" />


ℹ️ Tip: Validate that this group contains only the users you intend to include.


6. Complete the Import
After configuring the environment variables:

Review the summary screen
Start the import
Wait until the solution status shows Imported successfully

✅ The solution is now available in your environment.

7. Post‑Import Validation
After the import is complete, perform the following checks:

Ensure all flows are in an Enabled state
Verify that connection references are still active
Confirm environment variable values are correctly populated


8. Testing the Nudge App (Basic Validation)
To validate that the solution works as expected:

Trigger a sample flow manually (if provided)
Confirm:

The Adaptive Card is read correctly from SharePoint
Messages or nudges are sent as expected
Only users from the configured group receive notifications



✅ Always test in a non‑production environment first.

9. Best Practice Recommendations

Start with a small test group
Use development or sandbox environments
Apply your organisation’s governance and security controls
Monitor flow run history during testing


10. Support Disclaimer
This solution is provided as‑is:

No official Microsoft support is provided
No SLA or production guarantees are made
Users are responsible for adapting, validating, and supporting their own implementation
