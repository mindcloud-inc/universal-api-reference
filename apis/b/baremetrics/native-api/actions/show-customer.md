# Show Customer with Baremetrics

Retrieves a customer from Baremetrics.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/:source_id/customers/:oid`
- **Base URL:** `https://sandbox.baremetrics.com`
- **Official documentation:** [Show Customer](https://developers.baremetrics.com/reference/show-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `oid` | path | `string` | yes | — |
| `source_id` | path | `string` | yes | Please see [Sources](ref:sources) |
