# GPT Chatbot: Update Agent

Updates an existing agent in GPT Chatbot.

```
PUT https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/update-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GPT Chatbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/update-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentUuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/update-agent', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentUuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentUuid` | string | yes | Agent uuid. |
| `name` | string | no | Updated agent name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dataSourceUuids": [
        "string"
      ],
      "description": "string",
      "enabled": true,
      "meta": {},
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "prompt": "string",
      "toolFunctions": [
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
| `createdAt` | date |  |
| `dataSourceUuids` | array<string> |  |
| `description` | string |  |
| `enabled` | boolean |  |
| `meta` | object |  |
| `modifiedAt` | date |  |
| `name` | string |  |
| `prompt` | string |  |
| `toolFunctions` | array<object> |  |
| `type` | string |  |
| `uuid` | string |  |
| `variables` | array<object> |  |

## Native endpoint

Through the native GPT Chatbot API, this operation is `POST /agent/:uuid/update` (base URL `https://app.gptchatbot.it/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-agent.md) for the provider-specific parameters and requirements.

