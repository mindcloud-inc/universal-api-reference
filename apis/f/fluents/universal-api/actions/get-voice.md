# Fluents: Get Voice

Retrieves a voice from your Fluents account.

```
GET https://connect.mindcloud.co/v1/universal/fluents/latest/actions/get-voice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fluents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fluents/latest/actions/get-voice?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fluents/latest/actions/get-voice?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Fluents voice ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "api_key": "string",
      "description": "string",
      "experimental_input_streaming": true,
      "id": "string",
      "label": "string",
      "model_id": "string",
      "optimize_streaming_latency": 1,
      "similarity_boost": 1,
      "stability": 1,
      "type": "string",
      "user_id": "string",
      "voice_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `api_key` | string |  |
| `description` | string |  |
| `experimental_input_streaming` | boolean |  |
| `id` | string |  |
| `label` | string |  |
| `model_id` | string |  |
| `optimize_streaming_latency` | number |  |
| `similarity_boost` | number |  |
| `stability` | number |  |
| `type` | string |  |
| `user_id` | string |  |
| `voice_id` | string |  |

## Native endpoint

Through the native Fluents API, this operation is `GET /voices` (base URL `https://api.fluents.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-voice.md) for the provider-specific parameters and requirements.

