# SeaX: Send WABP Template Message

Sends a WhatsApp template message from SeaX.

```
POST https://connect.mindcloud.co/v1/universal/seaX/latest/actions/send-wabp-template-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seaX/latest/actions/send-wabp-template-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string",
  "templateLanguage": "string",
  "templateName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seaX/latest/actions/send-wabp-template-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "string",
    "templateLanguage": "string",
    "templateName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | yes | Conversation identifier. |
| `templateLanguage` | string | yes | Template language code. |
| `templateName` | string | yes | Template name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign_id": "string",
      "conversation_id": "string",
      "created_time": "string",
      "external_id": "string",
      "id": "string",
      "is_bot": true,
      "is_inbound": true,
      "message": "string",
      "message_time": "string",
      "segments_number": 1,
      "status": {},
      "updated_time": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign_id` | string |  |
| `conversation_id` | string |  |
| `created_time` | string |  |
| `external_id` | string |  |
| `id` | string |  |
| `is_bot` | boolean |  |
| `is_inbound` | boolean |  |
| `message` | string |  |
| `message_time` | string |  |
| `segments_number` | number |  |
| `status` | object |  |
| `updated_time` | string |  |

## Native endpoint

Through the native SeaX API, this operation is `POST /send_message/wabp_template_message` (base URL `https://seax.seasalt.ai/seax-api/api/v1/workspace/{{credentials.workspaceId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-wabp-template-message.md) for the provider-specific parameters and requirements.

