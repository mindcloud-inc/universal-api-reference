# Start playing a text-to-speech message to an active call with Routee

Starts playing a text-to-speech message to an active call in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/voice/conversation/:messageId/talk`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Start playing a text-to-speech message to an active call](https://docs.routee.net/reference/start-playing-a-text-to-speech-message-to-an-active-call)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The id of the voice call |
| `text` | body | `string` | yes | The text of the voice message to be played |
| `gender` | body | `string` | no | The gender of the voice message to be played. Check [here](/docs/text-to-speech) for possible values |
| `language` | body | `string` | no | The language of the voice message to be played. Check [here](/docs/text-to-speech) for possible values |
| `multiplex` | body | `boolean` | no | When set to true, the original audio is mixed together with the text-to-speech message. Default value false |
