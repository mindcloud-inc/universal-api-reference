# Botsonic: End Chat

Ends a chat conversation in Botsonic.

```
PUT https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/end-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botsonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/end-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatId": "550e8400-e29b-41d4-a716-446655440000"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/end-chat', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatId": "550e8400-e29b-41d4-a716-446655440000"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chatId` | string | yes | chat_id of the conversation to end. Example: `550e8400-e29b-41d4-a716-446655440000`. |
| `status` | string | no | Feedback status for the ended chat. Default: `none`. Example: `none`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `feedback` | string | no | Optional feedback for the chat. Example: `Conversation resolved successfully.`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Botsonic API returns.

## Native endpoint

Through the native Botsonic API, this operation is `POST /v1/business/bot-data/conversations/:chatId/end-chat` (base URL `https://api.botsonic.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/end-chat.md) for the provider-specific parameters and requirements.

