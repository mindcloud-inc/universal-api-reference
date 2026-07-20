# Hume AI: Stream Speech JSON

Streams synthesized speech from Hume AI as JSON.

```
POST https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/stream-speech-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hume AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/stream-speech-json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "utterances[0].text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/stream-speech-json', {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Hume AI API returns.

## Native endpoint

Through the native Hume AI API, this operation is `POST /v0/tts/stream/json` (base URL `https://api.hume.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stream-speech-json.md) for the provider-specific parameters and requirements.

