# Track Secure Message with DataMotion

Retrieves secure message tracking details from DataMotion.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.2/:transactionId/Track`
- **Base URL:** `https://api.datamotion.com/SecureMessageDelivery`
- **Official documentation:** [Track Secure Message](https://learn.microsoft.com/en-us/connectors/securemessagedelivery/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transactionId` | path | `string` | yes | Transaction ID of the secure message to track. |
