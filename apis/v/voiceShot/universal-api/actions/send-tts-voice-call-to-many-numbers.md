# VoiceShot: Send TTS Voice Call To Many Numbers

Creates TTS voice calls in VoiceShot for many recipients.

```
POST https://connect.mindcloud.co/v1/universal/voiceShot/latest/actions/send-tts-voice-call-to-many-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VoiceShot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voiceShot/latest/actions/send-tts-voice-call-to-many-numbers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "menuId": "string",
  "callerId": "string",
  "promptId": "string",
  "message": "string",
  "recipients[]": [
    {}
  ],
  "recipients[].number": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voiceShot/latest/actions/send-tts-voice-call-to-many-numbers', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "menuId": "string",
    "callerId": "string",
    "promptId": "string",
    "message": "string",
    "recipients[]": [{}],
    "recipients[].number": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `menuId` | string | yes | VoiceShot campaign identifier. |
| `callerId` | string | yes | Caller ID to display for all recipients. |
| `promptId` | string | yes | Prompt identifier inside the VoiceShot campaign. |
| `message` | string | yes | Text-to-speech message to speak for every recipient. |
| `transferTo` | string | no | Optional phone number to transfer recipients to. |
| `recipients[]` | array<object> | yes | Recipient list for the outbound call. |
| `recipients[].number` | string | yes | Destination phone number. |
| `recipients[].callId` | string | no | Optional client-defined call identifier. |
| `recipients[].countryCode` | string | no | Optional country code. |
| `recipients[].dateAndTime` | string | no | Optional scheduled delivery time. |

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

Through the native VoiceShot API, this operation is `POST /ivrapi.asp` (base URL `https://api.voiceshot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-tts-voice-call-to-many-numbers.md) for the provider-specific parameters and requirements.

