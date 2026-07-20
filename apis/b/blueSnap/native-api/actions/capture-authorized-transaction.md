# Capture Authorized Transaction with BlueSnap

Captures an authorized BlueSnap transaction.

## Endpoint

- **Method:** `PUT`
- **Path:** `/transactions`
- **Base URL:** `https://sandbox.bluesnap.com/services/2`
- **Official documentation:** [Capture Authorized Transaction](https://developers.bluesnap.com/v8976-JSON/reference/capture)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transactionId` | body | `string` | yes | Authorized transaction ID to capture. |
| `amount` | body | `string` | yes | Amount to capture. |
| `currency` | body | `string` | yes | Capture currency, e.g. USD. |
| `cardTransactionType` | body | `string` | yes | Use CAPTURE for this action. |
