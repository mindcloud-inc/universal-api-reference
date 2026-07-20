# Update Customer with Baremetrics

Updates a customer in Baremetrics.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/:source_id/customers/:customer_oid`
- **Base URL:** `https://sandbox.baremetrics.com`
- **Official documentation:** [Update Customer](https://developers.baremetrics.com/reference/update-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_oid` | path | `string` | yes | Your unique ID for the customer |
| `source_id` | path | `string` | yes | Please see [Sources](ref:sources) |
| `name` | body | `string` | no | — |
| `notes` | body | `string` | no | — |
| `created` | body | `string` | no | Unix timestamp of when this customer was created |
| `email` | body | `string` | no | Email for this customer |
