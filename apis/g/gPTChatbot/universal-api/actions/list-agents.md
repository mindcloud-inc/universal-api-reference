# GPT Chatbot: List Agents

Retrieves agents for a chatbot in GPT Chatbot.

```
GET https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/list-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GPT Chatbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/list-agents?connectionId=$CONNECTION_ID&chatbotUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatbotUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/list-agents?${params}`, {
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
| `chatbotUuid` | string | yes | Chatbot uuid. |

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

Through the native GPT Chatbot API, this operation is `GET /chatbot/:uuid/agents` (base URL `https://app.gptchatbot.it/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agents.md) for the provider-specific parameters and requirements.

