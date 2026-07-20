# Update Contact Custom Field with Constant Contact

Updates a contact custom field in Constant Contact.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contact_custom_fields/:custom_field_id`
- **Base URL:** `https://api.cc.email/v3`
- **Official documentation:** [Update Contact Custom Field](https://developer.constantcontact.com/api_guide/create_custom_fields.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `custom_field_id` | path | `string` | yes | The ID that uniquely identifies the custom field to update. |
| `label` | body | `string` | no | The custom field label to display. |
| `choices[]` | body | `array<object>` | no | Array of choice objects for single_select or multi_select fields. |
