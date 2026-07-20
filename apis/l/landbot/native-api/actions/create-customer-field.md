# Create Customer Field with Landbot

Creates a customer field in Landbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/customers/:customer_id/fields/:field_name/`
- **Base URL:** `https://api.landbot.io`
- **Official documentation:** [Create Customer Field](https://api.landbot.io/#api-CustomerFields-CreateField)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `number` | yes | Customer ID that owns the field. |
| `field_name` | path | `string` | yes | Field name to create on the customer. |
| `type` | body | `string` | no | Optional field type. Allowed values: string, integer, float, boolean, date, datetime. |
| `extra` | body | `object` | no | Optional extra field metadata object. |
| `value` | body | `string` | yes | Field value. Landbot accepts a value matching the selected type; this field is required. |
