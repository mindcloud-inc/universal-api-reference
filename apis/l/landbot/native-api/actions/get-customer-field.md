# Get Customer Field with Landbot

Retrieves a customer field from Landbot.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/customers/:customer_id/fields/:field_name/`
- **Base URL:** `https://api.landbot.io`
- **Official documentation:** [Get Customer Field](https://api.landbot.io/#api-CustomerFields-GetHttpsApiLandbotIoV1CustomersCustomer_idFieldsField_name)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `number` | yes | Customer ID that owns the field. |
| `field_name` | path | `string` | yes | Field name to retrieve from the customer. |
