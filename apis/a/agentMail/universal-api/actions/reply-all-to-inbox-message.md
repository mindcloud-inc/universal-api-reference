# Agent Mail: Reply All To Inbox Message

Replies to all recipients of an AgentMail message.

```
POST https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/reply-all-to-inbox-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/reply-all-to-inbox-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inboxId": "string",
  "messageId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/reply-all-to-inbox-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inboxId": "string",
    "messageId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inboxId` | string | yes | The AgentMail inbox ID. |
| `messageId` | string | yes | The AgentMail message ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message_id": "string",
      "thread_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message_id` | string | ID of the sent reply-all message. |
| `thread_id` | string | ID of the thread containing the reply. |

## Native endpoint

Through the native Agent Mail API, this operation is `POST /inboxes/{inbox_id}/messages/{message_id}/reply-all` (base URL `https://api.agentmail.to/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reply-all-to-inbox-message.md) for the provider-specific parameters and requirements.

