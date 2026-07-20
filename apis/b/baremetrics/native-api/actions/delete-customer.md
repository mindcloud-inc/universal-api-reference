# Delete Customer with Baremetrics

Deletes a customer from Baremetrics.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/:source_id/customers/:oid`
- **Base URL:** `https://sandbox.baremetrics.com`
- **Official documentation:** [Delete Customer](https://developers.baremetrics.com/reference/delete-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `oid` | path | `string` | yes | — |
| `source_id` | path | `string` | yes | Please see [Sources](ref:sources) |
