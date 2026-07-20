# Cancel Pending Request with Higgsfield AI

Cancels a pending generation request in Higgsfield AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/requests/{requestId}/cancel`
- **Base URL:** `https://platform.higgsfield.ai`
- **Official documentation:** [Cancel Pending Request](https://docs.higgsfield.ai/how-to/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestId` | path | `string` | yes | Queued Higgsfield request UUID to cancel. |
