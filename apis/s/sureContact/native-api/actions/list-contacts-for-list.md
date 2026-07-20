# List Contacts for List with SureContact

Retrieves contacts in a specific SureContact list.

## Endpoint

- **Method:** `GET`
- **Path:** `api/v1/public/lists/:list_uuid/contacts`
- **Base URL:** `https://api.surecontact.com`
- **Official documentation:** [List Contacts for List](https://api.surecontact.com/docs#list-management-GETapi-v1-public-lists--list_uuid--contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_uuid` | path | `string` | yes | The UUID of the list. |
