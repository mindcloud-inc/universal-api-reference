# Remove Contacts from List with SureContact

Removes contacts from an existing SureContact list.

## Endpoint

- **Method:** `POST`
- **Path:** `api/v1/public/lists/:list_uuid/contacts/remove`
- **Base URL:** `https://api.surecontact.com`
- **Official documentation:** [Remove Contacts from List](https://api.surecontact.com/docs#list-management-POSTapi-v1-public-lists--list_uuid--contacts-remove)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_uuids[]` | body | `array<string>` | yes | Array of contact UUIDs to remove from the list. |
| `list_uuid` | path | `string` | yes | The UUID of the list. |
