# Copy List with SureContact

Creates a copy of an existing SureContact list.

## Endpoint

- **Method:** `POST`
- **Path:** `api/v1/public/lists/:list_uuid/copy`
- **Base URL:** `https://api.surecontact.com`
- **Official documentation:** [Copy List](https://api.surecontact.com/docs#list-management-POSTapi-v1-public-lists--list_uuid--copy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_uuid` | path | `string` | yes | The UUID of the list. |
