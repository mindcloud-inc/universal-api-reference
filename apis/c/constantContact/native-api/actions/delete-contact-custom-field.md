# Delete Contact Custom Field with Constant Contact

Deletes a contact custom field from Constant Contact.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/contact_custom_fields/:custom_field_id`
- **Base URL:** `https://api.cc.email/v3`
- **Official documentation:** [Delete Contact Custom Field](https://developer.constantcontact.com/api_guide/delete_custom_fields.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `custom_field_id` | path | `string` | yes | The ID that uniquely identifies the custom field to delete. |
