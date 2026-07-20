# Chatvolt AI: Send Buttons

Sends interactive buttons through Chatvolt AI.

```
POST https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/whatsapp-send-buttons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/whatsapp-send-buttons" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string",
  "conversationId": "string",
  "body_text": "string",
  "button_1_id": "string",
  "button_1_title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/whatsapp-send-buttons', {
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
    "button_1_id": "string",
    "button_1_title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes | The ID of the agent sending the message. |
| `conversationId` | string | yes | The ID of the conversation. |
| `header_text` | string | no | Optional header text. |
| `body_text` | string | yes | The main message body. |
| `footer_text` | string | no | Optional footer text. |
| `button_1_id` | string | yes | ID for the first button. |
| `button_1_title` | string | yes | Label for the first button. |
| `button_2_id` | string | no | ID for the second button. |
| `button_2_title` | string | no | Label for the second button. |
| `button_3_id` | string | no | ID for the third button. |
| `button_3_title` | string | no | Label for the third button. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Chatvolt AI API returns.

## Native endpoint

Through the native Chatvolt AI API, this operation is `POST /messages/interactive/send-buttons` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/whatsapp-send-buttons.md) for the provider-specific parameters and requirements.

