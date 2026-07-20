# Stop playing a text-to-speech message to an active call with Routee

Stops playing a text-to-speech message to an active call in Routee.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/voice/conversation/:messageId/talk`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Stop playing a text-to-speech message to an active call](https://docs.routee.net/reference/stop-playing-a-text-to-speech-message-to-an-active-call)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The id of the voice call |
