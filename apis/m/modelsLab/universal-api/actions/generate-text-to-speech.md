# ModelsLab: Generate Text To Speech

Creates speech audio from text in ModelsLab.

```
POST https://connect.mindcloud.co/v1/universal/modelsLab/latest/actions/generate-text-to-speech
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ModelsLab `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/modelsLab/latest/actions/generate-text-to-speech" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/modelsLab/latest/actions/generate-text-to-speech', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prompt` | string | no | Text to convert to speech. |
| `voice_id` | string | no | Voice ID to use for speech generation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audio_time": 1,
      "generationTime": 1,
      "id": 1,
      "links": [
        "https://example.com"
      ],
      "message": "string",
      "output": [
        "string"
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audio_time` | number |  |
| `generationTime` | number |  |
| `id` | number |  |
| `links` | array<string> |  |
| `message` | string |  |
| `output` | array<string> |  |
| `status` | string |  |

## Native endpoint

Through the native ModelsLab API, this operation is `POST /v6/voice/text_to_speech` (base URL `https://modelslab.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-text-to-speech.md) for the provider-specific parameters and requirements.

