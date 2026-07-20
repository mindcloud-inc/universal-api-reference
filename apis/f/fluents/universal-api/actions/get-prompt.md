# Fluents: Get Prompt

Retrieves a prompt from your Fluents account.

```
GET https://connect.mindcloud.co/v1/universal/fluents/latest/actions/get-prompt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fluents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fluents/latest/actions/get-prompt?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fluents/latest/actions/get-prompt?${params}`, {
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
| `id` | string | yes | Fluents prompt ID. |

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

Through the native Fluents API, this operation is `GET /prompts` (base URL `https://api.fluents.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-prompt.md) for the provider-specific parameters and requirements.

