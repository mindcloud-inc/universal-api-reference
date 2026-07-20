# Fluents: Update Prompt

Updates an existing prompt in Fluents.

```
PUT https://connect.mindcloud.co/v1/universal/fluents/latest/actions/update-prompt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fluents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fluents/latest/actions/update-prompt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fluents/latest/actions/update-prompt', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Fluents prompt ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "collect_fields": {},
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
| `collect_fields` | object |  |
| `content` | string |  |
| `context_endpoint` | string |  |
| `description` | string |  |
| `id` | string |  |
| `label` | string |  |
| `prompt_template` | object |  |
| `type` | string |  |
| `user_id` | string |  |

## Native endpoint

Through the native Fluents API, this operation is `POST /prompts/update` (base URL `https://api.fluents.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-prompt.md) for the provider-specific parameters and requirements.

