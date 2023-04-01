# Linked Manager and Salesforce ID
Okta Workflows to set a linked manager and write the Salesforce ID to a users profile

Assumption: You are using the OIN Salesforce App with SCIM Provisioning enabled

Import two flows into Okta Workflows

Create a linked object attribute on the Okta Profile under Profile Editor for the Manager.
On the "Set Manager ID for Direct Report", update the attribute in options

Create an attribute on the Okta Profile in Profile Editor to hold the Salesforce ID.
Point the event to the SCIM enabled salesforce app in okta.
Update the app on the Get Users Salesforce ID card.

Set the manager attibute mapping to user.getLinkedObject("managerObject").salesforceID under Profile mapping for the Salesforce app in your okta tenant.
