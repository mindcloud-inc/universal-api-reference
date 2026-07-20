# Chatsistant: Update Agent

Updates an existing chatbot agent in Chatsistant.

```
PUT https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/update-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatsistant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/update-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/update-agent', {
  method: 'PUT',
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | The agent description. |
| `model` | string | no | The agent model. |
| `name` | string | no | The agent name. |
| `prompt` | string | no | The agent prompt. |
| `uuid` | string | no | The agent UUID. |

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

Through the native Chatsistant API, this operation is `POST /agent/:uuid/update` (base URL `https://app.chatsistant.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-agent.md) for the provider-specific parameters and requirements.

