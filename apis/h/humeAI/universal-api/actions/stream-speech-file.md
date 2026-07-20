# Hume AI: Stream Speech File

Streams synthesized speech from Hume AI as an audio file.

```
POST https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/stream-speech-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hume AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/stream-speech-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "utterances[0].text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/stream-speech-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "utterances[0].text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `utterances[0].text` | string | yes |  |
| `utterances[0].voice.name` | string | no |  |
| `utterances[0].voice.provider` | string | no |  |
| `utterances[0].description` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | Audio bytes. |
| `type` | string | Serialized buffer marker. |

## Native endpoint

Through the native Hume AI API, this operation is `POST /v0/tts/stream/file` (base URL `https://api.hume.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stream-speech-file.md) for the provider-specific parameters and requirements.

