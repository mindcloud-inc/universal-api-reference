# Get Transaction Payment Methods with Escrow.com

Retrieves transaction payment methods from Escrow.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/transaction/:transaction_id/payment_methods`
- **Base URL:** `https://api.escrow-sandbox.com/2017-09-01`
- **Official documentation:** [Get Transaction Payment Methods](https://www.escrow.com/api/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transaction_id` | path | `number` | yes | The Escrow.com transaction ID. |
