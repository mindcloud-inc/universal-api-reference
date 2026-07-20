# Request Replay Access with Dashcam

Requests access to a replay in Dashcam.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/replay/:replayId/access-request`
- **Base URL:** `https://api.testdriver.ai`
- **Official documentation:** [Request Replay Access](https://docs.testdriver.ai/v7/api/dashcam)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `replayId` | path | `string` | no |
| `requestEmail` | body | `string` | no |
| `requestMessage` | body | `string` | no |
| `shareKey` | body | `string` | no |
