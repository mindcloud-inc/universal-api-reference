# Runway: Voice Dubbing

Creates a voice dubbing task in Runway.

```
POST https://connect.mindcloud.co/v1/universal/runway/latest/actions/voice-dubbing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/runway/latest/actions/voice-dubbing" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "audioUri": "string",
  "model": "eleven_voice_dubbing",
  "targetLang": "es"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/runway/latest/actions/voice-dubbing', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "audioUri": "string",
    "model": "eleven_voice_dubbing",
    "targetLang": "es"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audioUri` | string | yes | HTTPS URL, Runway URI, or data URI for the source audio. |
| `disableVoiceCloning` | boolean | no | Whether to disable voice cloning and use a generic dubbed voice. |
| `dropBackgroundAudio` | boolean | no | Whether to remove background audio from the dubbed output. |
| `model` | string | yes | Runway currently requires eleven_voice_dubbing. Default: `eleven_voice_dubbing`. |
| `numSpeakers` | number | no | Optional number of detected speakers in the source audio. |
| `targetLang` | string | yes | Target dubbing language code, such as es, fr, or de. Default: `es`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "error": "string",
      "id": "string",
      "progress": 1,
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `error` | string |  |
| `id` | string |  |
| `progress` | number |  |
| `status` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Runway API, this operation is `POST /v1/voice_dubbing` (base URL `https://api.dev.runwayml.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/voice-dubbing.md) for the provider-specific parameters and requirements.

