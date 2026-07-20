# Sunshine Conversations: Post Message

Creates a new message in a Sunshine Conversations conversation.

```
POST https://connect.mindcloud.co/v1/universal/sunshineConversations/latest/actions/post-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sunshine Conversations `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sunshineConversations/latest/actions/post-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sunshineConversations/latest/actions/post-message', {
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
| `appId` | string | no | Sunshine Conversations app id. |
| `author` | string | no | Message author object. |
| `content` | string | no | Message content object. |
| `conversationId` | string | no | Conversation id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "messages": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `messages` | array<object> | Posted message records. |

## Native endpoint

Through the native Sunshine Conversations API, this operation is `POST /apps/:appId/conversations/:conversationId/messages` (base URL `https://api.smooch.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-message.md) for the provider-specific parameters and requirements.

