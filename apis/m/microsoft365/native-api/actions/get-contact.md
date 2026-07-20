# Get Contact with Microsoft 365

Retrieves a contact from Microsoft 365.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/contacts/{{contactId}}`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [Get Contact](https://learn.microsoft.com/en-us/graph/api/contact-get?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | The ID of the Outlook contact. |
