# Start recording an active call with Routee

Starts recording an active call in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/voice/conversation/:messageId/record`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Start recording an active call](https://docs.routee.net/reference/start-recording-an-active-call)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The id of the voice call |
| `duration` | body | `number` | no | The duration for each record that the user can perform |
| `format` | body | `string` | no | The record can have a format of  a "MP3" or a "WAV" file. |
