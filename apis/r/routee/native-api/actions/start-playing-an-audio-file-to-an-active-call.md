# Start playing an audio file to an active call with Routee

Starts playing an audio file to an active call in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/voice/conversation/:messageId/file`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Start playing an audio file to an active call](https://docs.routee.net/reference/start-playing-an-audio-file-to-an-active-call)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The id of the voice call |
| `fileURL` | body | `string` | yes | The url of the wav file to play |
| `multiplex` | body | `boolean` | no | When set to true, the original audio is mixed together with the played file. Default value false |
