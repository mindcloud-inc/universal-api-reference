# Add Contacts to List with SureContact

Adds contacts to an existing SureContact list.

## Endpoint

- **Method:** `POST`
- **Path:** `api/v1/public/lists/:list_uuid/contacts/add`
- **Base URL:** `https://api.surecontact.com`
- **Official documentation:** [Add Contacts to List](https://api.surecontact.com/docs#list-management-POSTapi-v1-public-lists--list_uuid--contacts-add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_uuids[]` | body | `array<string>` | yes | Array of contact UUIDs to add to the list. |
| `list_uuid` | path | `string` | yes | The UUID of the list. |
