# List Suppliers with Ascora

Retrieves suppliers from Ascora.

## Endpoint

- **Method:** `GET`
- **Path:** `/Suppliers/Suppliers`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [List Suppliers](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=64)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `BusinessNumber` | query | `string` | no | Performs an exact match against the Business Number of the Supplier, ignoring white space. |
| `SupplierName` | query | `string` | no | Performs a partial match against the Supplier Name. |
| `SupplierNumber` | query | `string` | no | Performs a partial match against the Supplier Number. |
