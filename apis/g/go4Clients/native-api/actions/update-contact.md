# Update Contact with Go4Clients

Updates an existing contact in Go4Clients.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/groupscontacts/contacts/v1.0`
- **Base URL:** `https://cloud.go4clients.com:8580`
- **Official documentation:** [Update Contact](https://apidoc.go4clients.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `_id` | body | `string` | yes | ID of the contact to update. |
| `mobileNumber` | body | `string` | yes | Contact phone number in international format. |
| `name` | body | `string` | no | Updated contact name. |
| `sex` | body | `string` | no | Updated contact sex field. |
| `weight` | body | `string` | no | Updated contact weight field. |
| `height` | body | `string` | no | Updated contact height field. |
