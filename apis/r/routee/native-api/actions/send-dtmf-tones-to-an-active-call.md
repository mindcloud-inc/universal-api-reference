# Send DTMF tones to an active call with Routee

Sends DTMF tones to an active call with Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/voice/conversation/:messageId/dtmf`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Send DTMF tones to an active call](https://docs.routee.net/reference/send-dtmf-tones-to-an-active-call)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The id of the voice call |
| `dtmf` | body | `string` | yes | A string with the dtmf tones to be sent. Valid characters are given by the regular expression: [A-D0-9#*,wW]+. The ',' and lowercase 'w' characters represents a half-second pause into the DTMF sequence, while the uppercase 'W' character represents one-second pause. |
