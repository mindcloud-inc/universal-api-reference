# Nvoip: Send Voice Blast



```
POST https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/send-voice-blast
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nvoip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/send-voice-blast" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "audios[]": [
    {}
  ],
  "audios[].audio": "string",
  "audios[].positionAudio": 1,
  "called": "string",
  "caller": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/send-voice-blast', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "audios[]": [{}],
    "audios[].audio": "string",
    "audios[].positionAudio": 1,
    "called": "string",
    "caller": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audios[]` | array<object> | yes | Array of audio instructions. |
| `audios[].audio` | string | yes | Audio file URL or identifier used in the voice message. |
| `audios[].positionAudio` | number | yes | Playback order for the audio item. |
| `called` | string | yes | Destino da chamada de voz. |
| `caller` | string | yes | Origem da chamada de voz. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "called": "string",
      "caller": "string",
      "callstart": "string",
      "dtmf": "string",
      "duration": "string",
      "reqend": "string",
      "reqstart": "string",
      "status": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `called` | string | Destination called number. |
| `caller` | string | Caller used for the voice blast. |
| `callstart` | string | Call start timestamp. |
| `dtmf` | string | DTMF capture payload returned by Nvoip. |
| `duration` | string | Call duration when present. |
| `reqend` | string | Request end timestamp. |
| `reqstart` | string | Request start timestamp. |
| `status` | string | Provider call status when present. |
| `uuid` | string | Provider voice blast identifier or route status. |

## Native endpoint

Through the native Nvoip API, this operation is `POST /torpedo/voice` (base URL `https://api.nvoip.com.br/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-voice-blast.md) for the provider-specific parameters and requirements.

