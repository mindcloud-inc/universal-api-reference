# List Customers with ECI Bolt

## Endpoint

- **Method:** `GET`
- **Path:** `/open/v1/customers`
- **Base URL:** `https://app.bolttech.net`
- **Official documentation:** [List Customers](https://app.bolttech.net/api-docs/index.html#/Customers/get_open_v1_customers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `refresh_token` | query | `string` | no | Token used to get the changed customers, returned on the last page of the customers. You should only send the refresh_token or the next_batch. |
| `refresh` | query | `string` | no | Return only directly changed records when value is "self" |
