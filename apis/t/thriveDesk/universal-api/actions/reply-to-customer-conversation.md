# ThriveDesk: Reply To Customer Conversation



```
POST https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/reply-to-customer-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThriveDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/reply-to-customer-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string",
  "customerEmail": "ava@example.com",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/reply-to-customer-conversation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "string",
    "customerEmail": "ava@example.com",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | yes | ThriveDesk customer conversation ID to reply to. |
| `customerEmail` | string | yes | Customer email address for the conversation reply. |
| `message` | string | yes | Reply message body. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "id": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Reply or conversation payload when returned. |
| `id` | string | Reply or conversation ID when returned. |
| `message` | string | Reply result message. |

## Native endpoint

Through the native ThriveDesk API, this operation is `POST /v1/customer/conversations/{{conversationId}}/reply` (base URL `https://api.thrivedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reply-to-customer-conversation.md) for the provider-specific parameters and requirements.

