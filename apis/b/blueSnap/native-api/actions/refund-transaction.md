# Refund Transaction with BlueSnap

Creates a refund for a BlueSnap transaction.

## Endpoint

- **Method:** `POST`
- **Path:** `/transactions/refund/:transactionId`
- **Base URL:** `https://sandbox.bluesnap.com/services/2`
- **Official documentation:** [Refund Transaction](https://developers.bluesnap.com/v8976-JSON/reference/refund)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transactionId` | path | `string` | yes | BlueSnap transaction ID to refund. |
| `amount` | body | `string` | yes | Refund amount, e.g. 1.00 |
