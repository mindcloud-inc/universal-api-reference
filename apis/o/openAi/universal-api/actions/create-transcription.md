# Open AI: Create Transcription

Transcribes audio in Open AI.

```
POST https://connect.mindcloud.co/v1/universal/openAi/latest/actions/create-transcription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/create-transcription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "model": "gpt-4o-mini-transcribe"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openAi/latest/actions/create-transcription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "model": "gpt-4o-mini-transcribe"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | Audio file input for transcription. |
| `model` | list | yes | Transcription model ID. Default: `gpt-4o-mini-transcribe`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "text": "string",
      "usage": {
        "seconds": 1,
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `text` | string |  |
| `usage.seconds` | number |  |
| `usage.type` | string |  |

## Native endpoint

Through the native Open AI API, this operation is `POST v1/audio/transcriptions` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transcription.md) for the provider-specific parameters and requirements.

