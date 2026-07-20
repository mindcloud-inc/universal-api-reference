# Create Custom Field with Quentn

## Endpoint

- **Method:** `POST`
- **Path:** `/custom-fields`
- **Base URL:** `https://tbg6y3.us-1.quentn.com/public/api/v1`
- **Official documentation:** [Create Custom Field](https://help.quentn.com/hc/en-150/articles/4518070370577-Custom-fields-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `label` | body | `string` | yes | Visible label of the custom field. |
| `field_type` | body | `string` | yes | Custom field type such as text, selection, date, integer, float, checkbox_confirmation, or url. |
| `description` | body | `string` | no | Optional description shown for the custom field. |
| `field_name` | body | `string` | no | Optional unique identifier. Quentn prefixes it with field_ automatically. |
| `max_length` | body | `number` | no | Optional max length for text fields. Allowed values include 8, 16, 32, 64, 128, and 255. |
