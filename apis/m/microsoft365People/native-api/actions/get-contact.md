# Get Contact with Microsoft 365 People

Retrieves a contact from Microsoft 365 People.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/contacts/{{contactId}}`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Get Contact](https://learn.microsoft.com/en-us/graph/api/contact-get?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | The ID of the Outlook contact. |
