# Sunshine Conversations: Post Activity

Posts conversation activity events to Sunshine Conversations.

```
POST https://connect.mindcloud.co/v1/universal/sunshineConversations/latest/actions/post-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sunshine Conversations `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sunshineConversations/latest/actions/post-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sunshineConversations/latest/actions/post-activity', {
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
| `activity` | string | no | Activity object. |
| `appId` | string | no | Sunshine Conversations app id. |
| `author` | string | no | Activity author object. |
| `conversationId` | string | no | Conversation id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activity": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activity` | object | Activity result. |
| `status` | string | Activity status. |

## Native endpoint

Through the native Sunshine Conversations API, this operation is `POST /apps/:appId/conversations/:conversationId/activity` (base URL `https://api.smooch.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-activity.md) for the provider-specific parameters and requirements.

