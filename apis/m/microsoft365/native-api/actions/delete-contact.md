# Delete Contact with Microsoft 365

Deletes a contact from Microsoft 365.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1.0/me/contacts/{{contactId}}`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [Delete Contact](https://learn.microsoft.com/en-us/graph/api/contact-delete?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | The ID of the Outlook contact to delete. |
