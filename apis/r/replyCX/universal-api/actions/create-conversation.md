# ReplyCX: Create Conversation



```
POST https://connect.mindcloud.co/v1/universal/replyCX/latest/actions/create-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReplyCX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/replyCX/latest/actions/create-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/replyCX/latest/actions/create-conversation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignee` | string | no |  |
| `channel` | string | no |  |
| `from` | string | no |  |
| `message.data.template` | string | no |  |
| `message.text` | string | no |  |
| `message.type` | string | no |  |
| `to.email` | string | no |  |
| `to.name` | string | no |  |
| `to.phone` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ReplyCX API returns.

## Native endpoint

Through the native ReplyCX API, this operation is `POST /api/v1/conversations` (base URL `https://api.reply.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-conversation.md) for the provider-specific parameters and requirements.

