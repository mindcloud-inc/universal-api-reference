# Delete Customer Custom Field with Quizell

Deletes a customer custom field from Quizell.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/customers/custom_fields/delete/:field_id`
- **Base URL:** `https://api.quizell.com/api/v1`
- **Official documentation:** [Delete Customer Custom Field](https://docs.quizell.com/customer-apis#delete-customers-custom-fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `field_id` | path | `number` | yes | ID of the custom field to delete. |
