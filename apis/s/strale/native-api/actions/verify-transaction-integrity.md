# Verify Transaction Integrity with Strale

Verifies a transaction integrity trail in Strale.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/verify/:transactionId`
- **Base URL:** `https://api.strale.io`
- **Official documentation:** [Verify Transaction Integrity](https://api.strale.io/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `depth` | query | `number` | no | Maximum chain depth to verify. |
| `transactionId` | path | `string` | yes | Transaction ID to verify. |
