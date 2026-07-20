# Get Transaction Disbursement Methods with Escrow.com

Retrieves transaction disbursement methods from Escrow.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/transaction/:transaction_id/disbursement_methods`
- **Base URL:** `https://api.escrow-sandbox.com/2017-09-01`
- **Official documentation:** [Get Transaction Disbursement Methods](https://www.escrow.com/api/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transaction_id` | path | `number` | yes | The Escrow.com transaction ID. |
