# Create Contact Custom Field with Constant Contact

Creates a contact custom field in Constant Contact.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact_custom_fields`
- **Base URL:** `https://api.cc.email/v3`
- **Official documentation:** [Create Contact Custom Field](https://developer.constantcontact.com/api_guide/create_custom_fields.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `label` | body | `string` | yes | Custom field label shown in the Constant Contact UI. |
| `type` | body | `string` | yes | Data value type for the custom field. |
| `metadata` | body | `object` | no | Display and validation metadata object for the custom field. |
| `choices[]` | body | `array<object>` | no | Choices array for single_select or multi_select field types. |
| `version` | body | `number` | no | Datetime version for date fields (1 legacy string, 2 native date). |
