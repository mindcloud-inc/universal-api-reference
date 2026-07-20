# Stop playing an audio file to an active call with Routee

Stops playing an audio file to an active call in Routee.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/voice/conversation/:messageId/file`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Stop playing an audio file to an active call](https://docs.routee.net/reference/stop-playing-an-audio-file-to-an-active-call)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The id of the voice call. |
