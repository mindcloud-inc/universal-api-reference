# Retract Secure Message with DataMotion

Retracts a previously sent secure message in DataMotion.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1.2/:transactionId/Retract`
- **Base URL:** `https://api.datamotion.com/SecureMessageDelivery`
- **Official documentation:** [Retract Secure Message](https://learn.microsoft.com/en-us/connectors/securemessagedelivery/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transactionId` | path | `string` | yes | Transaction ID of the secure message to retract. |
