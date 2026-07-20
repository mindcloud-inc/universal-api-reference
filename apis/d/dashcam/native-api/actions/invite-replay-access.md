# Invite Replay Access with Dashcam

Invites a user to access a replay in Dashcam.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/replay/:replayId/access-invite`
- **Base URL:** `https://api.testdriver.ai`
- **Official documentation:** [Invite Replay Access](https://docs.testdriver.ai/v7/api/dashcam)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | no |
| `replayId` | path | `string` | no |
