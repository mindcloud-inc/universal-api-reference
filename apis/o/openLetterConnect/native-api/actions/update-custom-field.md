# Update Custom Field with Open Letter Connect

Updates a custom field in Open Letter Connect.

## Endpoint

- **Method:** `PUT`
- **Path:** `/custom-fields/:id`
- **Base URL:** `https://api.openletterconnect.com/api/v1`
- **Official documentation:** [Update Custom Field](https://api-docs.openletterconnect.com/custom-fields/update-custom-field/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customFieldName` | body | `string` | yes | The custom field label to save. |
| `id` | path | `number` | yes | The numeric custom field ID from Open Letter Connect. |
