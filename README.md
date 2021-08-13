# TOPdesk-Assign-Asset-Business-Owner
Assign a change approval to the business owner

Summary:
The owner, of the asset linked to the change, is assigned to the authorization activity. On a given change with an asset linked, look up who owns the asset, and assign the authorization activity manager to the asset owner

Use Case:
When doing patches/updates/maintenance to a particular asset, it is valuable to notify the manager/owner of that asset of the upcoming disruption & change. Then you need to get the asset owner’s approval. In an extensive change workflow, you can insert an authorization activity to get approval from a manager before proceeding with the change. This action sequence looks up the owner of the asset linked to the change, and assigns them as the authorization activity manager. An example would be getting approval from the server owner on the restart time, before doing maintenance on a server. Another example would be getting approval from the application manager before updating an application.

Explanation of Steps:Step 1 – Get asset linked to the change. This looks up the asset that is linked to the change. Step 2 – Get asset assignments. This looks at the linked asset’s assignee. Step 3 – Assign authorization activity to asset assignee. This takes the person from the previous step and assigns them as the authorization activity manager.

Permissions for API Operator:
1.	API: REST API - Read, Application Passwords - Write.
2.	Change Management: Extensive Changes - Read & Write, Authorization Activities - Read & write.
3.	Supporting Files: Persons - Read

Variables:
1.	TOPdesk_user: The Operator account used to perform this action (e.g. ADMIN).
2.	TOPdesk_applicationpassword: Application password configured for the API user/operator.
3.	topdesk_url: URL to your TOPdesk environment.

Extended Notes:
This action sequence only works if there is one authorization activity in the extensive change, and if there is only one person assigned to the asset.

