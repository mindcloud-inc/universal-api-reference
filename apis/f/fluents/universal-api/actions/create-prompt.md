# Fluents: Create Prompt

Creates a new prompt in Fluents.

```
POST https://connect.mindcloud.co/v1/universal/fluents/latest/actions/create-prompt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fluents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fluents/latest/actions/create-prompt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fluents/latest/actions/create-prompt', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "collect_fields": [
        "string"
      ],
      "content": "string",
      "context_endpoint": "string",
      "description": "string",
      "id": "string",
      "label": "string",
      "prompt_template": {},
      "type": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collect_fields` | array<string> |  |
| `content` | string |  |
| `context_endpoint` | string |  |
| `description` | string |  |
| `id` | string |  |
| `label` | string |  |
| `prompt_template` | object |  |
| `type` | string |  |
| `user_id` | string |  |

## Native endpoint

Through the native Fluents API, this operation is `POST /prompts/create` (base URL `https://api.fluents.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-prompt.md) for the provider-specific parameters and requirements.

