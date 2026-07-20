# Website Toolbox Community: Create Message



```
POST https://connect.mindcloud.co/v1/universal/websiteToolboxCommunity/latest/actions/create-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Website Toolbox Community `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/websiteToolboxCommunity/latest/actions/create-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/websiteToolboxCommunity/latest/actions/create-message', {
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
      "body": "string",
      "conversationId": 1,
      "messageId": 1,
      "object": "string",
      "timestamp": 1,
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
| `body` | string |  |
| `conversationId` | number |  |
| `messageId` | number |  |
| `object` | string |  |
| `timestamp` | number |  |
| `userId` | number |  |
| `username` | string |  |

## Native endpoint

Through the native Website Toolbox Community API, this operation is `POST /api/conversations/:conversationId/messages` (base URL `https://api.websitetoolbox.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-message.md) for the provider-specific parameters and requirements.

