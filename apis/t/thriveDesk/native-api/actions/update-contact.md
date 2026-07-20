# Update Contact with ThriveDesk

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/contacts/{{contactId}}`
- **Base URL:** `https://api.thrivedesk.com`
- **Official documentation:** [Update Contact](https://wordpress.org/plugins/thrivedesk/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | ThriveDesk contact ID to update. |
| `name` | body | `string` | no | Updated contact name. |
| `email` | body | `string` | yes | Updated contact email address. |
