# Disable Customer with Finmo

Disables an existing customer in Finmo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/customer/:customer_id/disable`
- **Base URL:** `https://api.finmo.net/v1/`
- **Official documentation:** [Disable Customer](https://docs.finmo.net/reference/disablecustomer-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `string` | yes | Customer identifier to disable. |
