# QWIC: Close Conversation

Closes a QWIC conversation.

```
PUT https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/close-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QWIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/close-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversation_id": "string",
  "user.by": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/close-conversation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversation_id": "string",
    "user.by": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversation_id` | string | yes | The QWIC conversation identifier. |
| `user.by` | string | yes | The agent email closing the conversation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native QWIC API, this operation is `POST /api/v1/conversation/:conversation_id/events` (base URL `https://app.qwic.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/close-conversation.md) for the provider-specific parameters and requirements.

