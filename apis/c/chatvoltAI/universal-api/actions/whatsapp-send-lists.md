# Chatvolt AI: Send List

Sends an interactive list through Chatvolt AI.

```
POST https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/whatsapp-send-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/whatsapp-send-lists" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string",
  "conversationId": "string",
  "body_text": "string",
  "button_text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/whatsapp-send-lists', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string",
    "conversationId": "string",
    "body_text": "string",
    "button_text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes | The ID of the agent. |
| `conversationId` | string | yes | The ID of the conversation. |
| `header_text` | string | no | Optional header text. |
| `body_text` | string | yes | Main message body. |
| `footer_text` | string | no | Optional footer text. |
| `button_text` | string | yes | Text for the button that opens the list. |
| `list_title` | string | no | Title for the list (mainly for Z-API). |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Chatvolt AI API returns.

## Native endpoint

Through the native Chatvolt AI API, this operation is `POST /messages/interactive/send-lists` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/whatsapp-send-lists.md) for the provider-specific parameters and requirements.

