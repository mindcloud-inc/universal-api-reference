# Enrich Dispute with Chargeflow

Enriches an existing dispute in Chargeflow.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/disputes/{disputeId}`
- **Base URL:** `https://api.chargeflow.io/public/2025-04-01`
- **Official documentation:** [Enrich Dispute](https://docs.chargeflow.io/reference/patch_public-2025-04-01-disputes-disputeid-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `disputeId` | path | `string` | yes | The Chargeflow dispute ID. |
