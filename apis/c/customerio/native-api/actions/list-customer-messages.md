# List Customer Messages with Customer.io

Retrieves messages sent to a customer in Customer.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/customers/:customer_id/messages`
- **Base URL:** `https://api.customer.io`
- **Official documentation:** [List Customer Messages](https://docs.customer.io/integrations/api/app/#tag/Customers/operation/getPersonMessages)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `string` | yes | The ID of the customer to inspect. |
| `id_type` | query | `list<string>` | no | The type of identifier provided in Customer ID. Accepted values: `cio_id`, `email`, `id`. |
| `start_ts` | query | `date` | no | The beginning timestamp for the query. |
| `end_ts` | query | `date` | no | The ending timestamp for the query. |
