# Website Toolbox Community: Update Topic



```
PUT https://connect.mindcloud.co/v1/universal/websiteToolboxCommunity/latest/actions/update-topic
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Website Toolbox Community `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/websiteToolboxCommunity/latest/actions/update-topic" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/websiteToolboxCommunity/latest/actions/update-topic', {
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
      "locked": true,
      "object": "string",
      "pinned": true,
      "postCount": 1,
      "subject": "string",
      "topicId": 1,
      "viewCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryId` | number |  |
| `locked` | boolean |  |
| `object` | string |  |
| `pinned` | boolean |  |
| `postCount` | number |  |
| `subject` | string |  |
| `topicId` | number |  |
| `viewCount` | number |  |

## Native endpoint

Through the native Website Toolbox Community API, this operation is `POST /api/topics/:topicId` (base URL `https://api.websitetoolbox.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-topic.md) for the provider-specific parameters and requirements.

