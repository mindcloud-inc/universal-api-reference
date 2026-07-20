# Chatsistant: List Agents

Retrieves chatbot agent records from Chatsistant.

```
GET https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/list-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatsistant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/list-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/list-agents?${params}`, {
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
| `uuid` | string | no | The chatbot UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "data_source_uuids": [
        "string"
      ],
      "description": "string",
      "enabled": true,
      "meta": {},
      "modified_at": "string",
      "name": "Ava Chen",
      "prompt": "string",
      "tool_functions": [
        {}
      ],
      "type": "string",
      "uuid": "string",
      "variables": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `data_source_uuids` | array<string> |  |
| `description` | string |  |
| `enabled` | boolean |  |
| `meta` | object |  |
| `modified_at` | string |  |
| `name` | string |  |
| `prompt` | string |  |
| `tool_functions` | array<object> |  |
| `type` | string |  |
| `uuid` | string |  |
| `variables` | array<object> |  |

## Native endpoint

Through the native Chatsistant API, this operation is `GET /chatbot/:uuid/agents` (base URL `https://app.chatsistant.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agents.md) for the provider-specific parameters and requirements.

