# Website Toolbox Community: Create Conversation



```
POST https://connect.mindcloud.co/v1/universal/websiteToolboxCommunity/latest/actions/create-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Website Toolbox Community `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/websiteToolboxCommunity/latest/actions/create-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/websiteToolboxCommunity/latest/actions/create-conversation', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "conversationId": 1,
      "messageCount": 1,
      "object": "string",
      "subject": "string",
      "timestamp": 1,
      "topicId": 1,
      "userId": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversationId` | number |  |
| `messageCount` | number |  |
| `object` | string |  |
| `subject` | string |  |
| `timestamp` | number |  |
| `topicId` | number |  |
| `userId` | number |  |
| `username` | string |  |

## Native endpoint

Through the native Website Toolbox Community API, this operation is `POST /api/conversations` (base URL `https://api.websitetoolbox.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-conversation.md) for the provider-specific parameters and requirements.

