# Website Toolbox Community: Update Post



```
PUT https://connect.mindcloud.co/v1/universal/websiteToolboxCommunity/latest/actions/update-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Website Toolbox Community `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/websiteToolboxCommunity/latest/actions/update-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/websiteToolboxCommunity/latest/actions/update-post', {
  method: 'PUT',
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
      "categoryId": 1,
      "message": "string",
      "object": "string",
      "postId": 1,
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
| `categoryId` | number |  |
| `message` | string |  |
| `object` | string |  |
| `postId` | number |  |
| `subject` | string |  |
| `timestamp` | number |  |
| `topicId` | number |  |
| `userId` | number |  |
| `username` | string |  |

## Native endpoint

Through the native Website Toolbox Community API, this operation is `POST /api/posts/:postId` (base URL `https://api.websitetoolbox.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-post.md) for the provider-specific parameters and requirements.

