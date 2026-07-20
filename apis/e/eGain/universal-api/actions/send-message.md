# eGain: Send Message

Sends conversation messages in eGain Conversation Hub.

```
POST https://connect.mindcloud.co/v1/universal/eGain/latest/actions/send-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eGain/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messages.message[0].content.text": "string",
  "messages.message[0].conversation.account.address": "string",
  "messages.message[0].conversation.account.channel.type": "string",
  "messages.message[0].conversation.customer.contacts.contact[0].address": "string",
  "messages.message[0].conversation.customer.contacts.contact[0].type": "string",
  "messages.message[0].conversation.entryPoint.id": "string",
  "messages.message[0].sender.type": "string",
  "messages.message[0].type.value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eGain/latest/actions/send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messages.message[0].content.text": "string",
    "messages.message[0].conversation.account.address": "string",
    "messages.message[0].conversation.account.channel.type": "string",
    "messages.message[0].conversation.customer.contacts.contact[0].address": "string",
    "messages.message[0].conversation.customer.contacts.contact[0].type": "string",
    "messages.message[0].conversation.entryPoint.id": "string",
    "messages.message[0].sender.type": "string",
    "messages.message[0].type.value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messages.message[0].content` | string | no | Raw message content object. |
| `messages.message[0].content.text` | string | yes | Text message content. |
| `messages.message[0].conversation.account.address` | string | yes | Conversation account address. |
| `messages.message[0].conversation.account.channel.type` | string | yes | Channel type for the conversation account. |
| `messages.message[0].conversation.customer.contacts.contact[0].address` | string | yes | Customer contact address. |
| `messages.message[0].conversation.customer.contacts.contact[0].type` | string | yes | Customer contact type. |
| `messages.message[0].conversation.entryPoint.id` | string | yes | Entry point ID for the conversation. |
| `messages.message[0].sender.type` | string | yes | Sender client type. |
| `messages.message[0].type.value` | string | yes | Message type value. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native eGain API returns.

## Native endpoint

Through the native eGain API, this operation is `POST /conversations/messages` (base URL `https://api.ai.egain.cloud/conversation/conversationmgr/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message.md) for the provider-specific parameters and requirements.

