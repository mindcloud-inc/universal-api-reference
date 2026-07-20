# Get Customer with Finmo

Finds a customer in Finmo by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/customer/:customer`
- **Base URL:** `https://api.finmo.net/v1/`
- **Official documentation:** [Get Customer](https://docs.finmo.net/reference/getcustomerbyid-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer` | path | `string` | yes | Customer identifier to retrieve. |
| `include_deleted` | query | `boolean` | no | Include deleted customers in the lookup. |
