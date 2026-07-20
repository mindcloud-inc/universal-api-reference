# Upload Evidence with Chargeflow

Uploads evidence for an existing dispute in Chargeflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/disputes/{disputeId}/evidence`
- **Base URL:** `https://api.chargeflow.io/public/2025-04-01`
- **Official documentation:** [Upload Evidence](https://docs.chargeflow.io/reference/post_public-2025-04-01-disputes-disputeid-evidence-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `disputeId` | path | `string` | yes | The Chargeflow dispute ID. |
