# Reverse Authorized Transaction with BlueSnap

Reverses an authorized BlueSnap transaction.

## Endpoint

- **Method:** `PUT`
- **Path:** `/transactions`
- **Base URL:** `https://sandbox.bluesnap.com/services/2`
- **Official documentation:** [Reverse Authorized Transaction](https://developers.bluesnap.com/v8976-JSON/reference/auth-reversal)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transactionId` | body | `string` | yes | Authorized transaction ID to reverse. |
