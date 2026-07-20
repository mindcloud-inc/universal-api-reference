# VoiceShot: Send TTS Voice Call To One Number

Creates a TTS voice call in VoiceShot.

```
POST https://connect.mindcloud.co/v1/universal/voiceShot/latest/actions/send-tts-voice-call-to-one-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VoiceShot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voiceShot/latest/actions/send-tts-voice-call-to-one-number" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "menuId": "string",
  "callerId": "string",
  "number": "string",
  "promptId": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voiceShot/latest/actions/send-tts-voice-call-to-one-number', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "menuId": "string",
    "callerId": "string",
    "number": "string",
    "promptId": "string",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `menuId` | string | yes | VoiceShot campaign identifier. |
| `callerId` | string | yes | Caller ID to display for the outbound call. |
| `number` | string | yes | Destination phone number. |
| `promptId` | string | yes | Prompt identifier inside the VoiceShot campaign. |
| `message` | string | yes | Text-to-speech message to speak. |
| `callId` | string | no | Optional client-defined call identifier. |
| `countryCode` | string | no | Optional country code for the destination number. |
| `dateAndTime` | string | no | Optional scheduled delivery time. |
| `transferTo` | string | no | Optional phone number to transfer the recipient to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "errorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string | VoiceShot response comment or error message. |
| `errorId` | string | VoiceShot response error code. 0 means ok. |

## Native endpoint

Through the native VoiceShot API, this operation is `POST /ivrapi.asp` (base URL `https://api.voiceshot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-tts-voice-call-to-one-number.md) for the provider-specific parameters and requirements.

