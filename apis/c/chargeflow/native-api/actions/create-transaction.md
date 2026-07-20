# Create Transaction with Chargeflow

Creates a new dispute transaction in Chargeflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/disputes/{disputeId}/transaction`
- **Base URL:** `https://api.chargeflow.io/public/2025-04-01`
- **Official documentation:** [Create Transaction](https://docs.chargeflow.io/reference/transaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `disputeId` | path | `string` | yes | The Chargeflow dispute ID. |
