# AI/ML API: Create Speech With TTS-1 HD

Creates speech with TTS-1 HD in AI/ML API.

```
POST https://connect.mindcloud.co/v1/universal/aIMLAPI/latest/actions/create-speech-with-tts1-hd
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AI/ML API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aIMLAPI/latest/actions/create-speech-with-tts1-hd" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aIMLAPI/latest/actions/create-speech-with-tts1-hd', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `text` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `responseFormat` | string | no | Default: `mp3`. |
| `speed` | number | no | Default: `1`. |
| `style` | string | no |  |
| `voice` | string | no | Default: `alloy`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AI/ML API API returns.

## Native endpoint

Through the native AI/ML API API, this operation is `POST /v1/tts` (base URL `https://api.aimlapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-speech-with-tts1-hd.md) for the provider-specific parameters and requirements.

