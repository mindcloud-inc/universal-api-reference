# Website Toolbox Community: Get Topic



```
GET https://connect.mindcloud.co/v1/universal/websiteToolboxCommunity/latest/actions/get-topic
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Website Toolbox Community `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/websiteToolboxCommunity/latest/actions/get-topic?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/websiteToolboxCommunity/latest/actions/get-topic?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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
      "lastPost": {},
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
| `lastPost` | object |  |
| `locked` | boolean |  |
| `object` | string |  |
| `pinned` | boolean |  |
| `postCount` | number |  |
| `subject` | string |  |
| `topicId` | number |  |
| `viewCount` | number |  |

## Native endpoint

Through the native Website Toolbox Community API, this operation is `GET /api/topics/:topicId` (base URL `https://api.websitetoolbox.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-topic.md) for the provider-specific parameters and requirements.

