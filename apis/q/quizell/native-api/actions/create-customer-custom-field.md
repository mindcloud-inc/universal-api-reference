# Create Customer Custom Field with Quizell

Creates a customer custom field in Quizell.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/custom_fields/store`
- **Base URL:** `https://api.quizell.com/api/v1`
- **Official documentation:** [Create Customer Custom Field](https://docs.quizell.com/customer-apis#create-customers-custom-fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `field_name` | body | `string` | yes | Name or label of the custom field. |
| `field_type` | body | `string` | yes | Type of field (text, textarea, select, checkbox, radio). |
