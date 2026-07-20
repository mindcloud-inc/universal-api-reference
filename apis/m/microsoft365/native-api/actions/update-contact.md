# Update Contact with Microsoft 365

Updates a contact in Microsoft 365.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1.0/me/contacts/{{contactId}}`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [Update Contact](https://learn.microsoft.com/en-us/graph/api/contact-update?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | The ID of the Outlook contact to update. |
| `displayName` | body | `string` | no | Updated display name for the contact. |
| `givenName` | body | `string` | no | Updated given name for the contact. |
| `surname` | body | `string` | no | Updated surname for the contact. |
| `emailAddresses[].name` | body | `string` | no | Updated display name for the primary email address. |
| `emailAddresses[].address` | body | `string` | no | Updated primary email address for the contact. |
| `companyName` | body | `string` | no | Updated company name for the contact. |
| `jobTitle` | body | `string` | no | Updated job title for the contact. |
| `mobilePhone` | body | `string` | no | Updated mobile phone number for the contact. |
