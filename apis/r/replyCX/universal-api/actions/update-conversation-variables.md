# ReplyCX: Update Conversation Variables



```
PUT https://connect.mindcloud.co/v1/universal/replyCX/latest/actions/update-conversation-variables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReplyCX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/replyCX/latest/actions/update-conversation-variables" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string",
  "variables": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/replyCX/latest/actions/update-conversation-variables', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "string",
    "variables": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | yes |  |
| `variables` | list<object> | yes | List of variable objects with keys name, type, and value. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ReplyCX API returns.

## Native endpoint

Through the native ReplyCX API, this operation is `POST /v1/accounts/:account_id/conversations/:conversation_id/variables` (base URL `https://api.reply.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-conversation-variables.md) for the provider-specific parameters and requirements.

