# Update Customer with MRPeasy

Updates an existing customer in MRPeasy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/customers/{{customerId}}`
- **Base URL:** `https://api.mrpeasy.com/rest/v1`
- **Official documentation:** [Update Customer](https://www.mrpeasy.com/resources/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `number` | yes | MRPeasy customer ID. |
| `title` | body | `string` | no | Updated customer title. |
| `code` | body | `string` | no | Updated customer code. |
| `contact_data` | body | `array<object>` | no | Updated MRPeasy contact_data array. |
