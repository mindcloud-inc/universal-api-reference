# Sunshine Conversations: Create Conversation

Creates a new conversation in Sunshine Conversations.

```
POST https://connect.mindcloud.co/v1/universal/sunshineConversations/latest/actions/create-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sunshine Conversations `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sunshineConversations/latest/actions/create-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sunshineConversations/latest/actions/create-conversation', {
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
| `displayName` | string | no | Conversation display name. |
| `participants` | string | no | Conversation participants array. |
| `type` | string | no | Conversation type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversation": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversation` | object | Created conversation. |

## Native endpoint

Through the native Sunshine Conversations API, this operation is `POST /apps/:appId/conversations` (base URL `https://api.smooch.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-conversation.md) for the provider-specific parameters and requirements.

