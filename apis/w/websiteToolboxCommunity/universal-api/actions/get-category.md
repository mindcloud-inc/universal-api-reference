# Website Toolbox Community: Get Category



```
GET https://connect.mindcloud.co/v1/universal/websiteToolboxCommunity/latest/actions/get-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Website Toolbox Community `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/websiteToolboxCommunity/latest/actions/get-category?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/websiteToolboxCommunity/latest/actions/get-category?${params}`, {
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
      "description": "string",
      "heading": "string",
      "isPrivate": true,
      "lastPost": {},
      "linked": "https://example.com",
      "locked": true,
      "object": "string",
      "parentId": 1,
      "passwordProtected": true,
      "replyCount": 1,
      "title": "string",
      "topicCount": 1,
      "unlisted": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryId` | number |  |
| `description` | string |  |
| `heading` | string |  |
| `isPrivate` | boolean |  |
| `lastPost` | object |  |
| `linked` | string |  |
| `locked` | boolean |  |
| `object` | string |  |
| `parentId` | number |  |
| `passwordProtected` | boolean |  |
| `replyCount` | number |  |
| `title` | string |  |
| `topicCount` | number |  |
| `unlisted` | boolean |  |

## Native endpoint

Through the native Website Toolbox Community API, this operation is `GET /api/categories/:categoryId` (base URL `https://api.websitetoolbox.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-category.md) for the provider-specific parameters and requirements.

