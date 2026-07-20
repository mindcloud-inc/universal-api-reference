# Get Transaction with Escrow.com

Retrieves a transaction from Escrow.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/transaction/:transaction_id`
- **Base URL:** `https://api.escrow-sandbox.com/2017-09-01`
- **Official documentation:** [Get Transaction](https://www.escrow.com/api/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transaction_id` | path | `number` | yes | The Escrow.com transaction ID. |
