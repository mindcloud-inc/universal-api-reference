# Get Transaction by Reference with Escrow.com

Retrieves a transaction from Escrow.com by reference.

## Endpoint

- **Method:** `GET`
- **Path:** `/transaction/reference/:reference`
- **Base URL:** `https://api.escrow-sandbox.com/2017-09-01`
- **Official documentation:** [Get Transaction by Reference](https://www.escrow.com/api/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reference` | path | `string` | yes | The external reference for the transaction. |
