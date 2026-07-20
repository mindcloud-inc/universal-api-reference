# Enable Customer with Finmo

Enables an existing customer in Finmo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/customer/:customer_id/enable`
- **Base URL:** `https://api.finmo.net/v1/`
- **Official documentation:** [Enable Customer](https://docs.finmo.net/reference/enablecustomer-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `string` | yes | Customer identifier to enable. |
