# Get Request Status with Higgsfield AI

Retrieves a generation request status from Higgsfield AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/requests/{requestId}/status`
- **Base URL:** `https://platform.higgsfield.ai`
- **Official documentation:** [Get Request Status](https://docs.higgsfield.ai/how-to/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestId` | path | `string` | yes | Higgsfield request UUID returned by a generation request. |
