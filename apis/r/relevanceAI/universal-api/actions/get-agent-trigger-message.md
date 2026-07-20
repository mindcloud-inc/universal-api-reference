# Relevance AI: Get Agent Trigger Message



```
GET https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/get-agent-trigger-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Relevance AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/get-agent-trigger-message?connectionId=$CONNECTION_ID&agentId=string&conversationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentId": "string",
  "conversationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/get-agent-trigger-message?${params}`, {
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
| `agentId` | string | yes | The Relevance AI agent id. |
| `conversationId` | string | yes | The task or conversation id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "trigger_message": {
        "content": {
          "display": {
            "name": "Ava Chen"
          },
          "text": "string",
          "trigger_source": "string"
        },
        "insert_date_": "2026-05-07T12:00:00.000Z",
        "item_id": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `trigger_message.content.display.name` | string | The display name on the trigger message. |
| `trigger_message.content.text` | string | The trigger message text. |
| `trigger_message.content.trigger_source` | string | The trigger source. |
| `trigger_message.insert_date_` | date | When the trigger message was created. |
| `trigger_message.item_id` | string | The trigger message item ID. |

## Native endpoint

Through the native Relevance AI API, this operation is `GET /agents/:agentId/tasks/:conversationId/trigger_message` (base URL `https://api-{{credentials.region}}.stack.tryrelevance.com/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent-trigger-message.md) for the provider-specific parameters and requirements.

