# Freepik: Improve Prompt



```
POST https://connect.mindcloud.co/v1/universal/freepik/latest/actions/improve-prompt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freepik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freepik/latest/actions/improve-prompt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "A detailed photo of a sunlit forest path",
  "type": "image"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freepik/latest/actions/improve-prompt', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prompt": "A detailed photo of a sunlit forest path",
    "type": "image"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prompt` | string | yes | Prompt text to improve. Default: `A detailed photo of a sunlit forest path`. |
| `type` | list | yes | Prompt type to improve: image or video. One of: `image`, `video`. Default: `image`. |
| `language` | string | no | Two-letter output language code. Default: `en`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "generated": [
        {}
      ],
      "status": "string",
      "task_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `generated` | array<object> | Generated improved prompt results when ready. |
| `status` | string | Task status. |
| `task_id` | string | Prompt improvement task ID. |

## Native endpoint

Through the native Freepik API, this operation is `POST /v1/ai/improve-prompt` (base URL `https://api.freepik.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/improve-prompt.md) for the provider-specific parameters and requirements.

