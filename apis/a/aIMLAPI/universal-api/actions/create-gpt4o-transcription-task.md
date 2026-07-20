# AI/ML API: Create GPT-4o Transcription Task

Creates a GPT-4o transcription task in AI/ML API.

```
POST https://connect.mindcloud.co/v1/universal/aIMLAPI/latest/actions/create-gpt4o-transcription-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AI/ML API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aIMLAPI/latest/actions/create-gpt4o-transcription-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aIMLAPI/latest/actions/create-gpt4o-transcription-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language` | string | no |  |
| `prompt` | string | no |  |
| `temperature` | number | no | Default: `0`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AI/ML API API returns.

## Native endpoint

Through the native AI/ML API API, this operation is `POST /v1/stt/create` (base URL `https://api.aimlapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-gpt4o-transcription-task.md) for the provider-specific parameters and requirements.

