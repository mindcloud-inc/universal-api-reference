# Website Toolbox Community: Update Category



```
PUT https://connect.mindcloud.co/v1/universal/websiteToolboxCommunity/latest/actions/update-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Website Toolbox Community `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/websiteToolboxCommunity/latest/actions/update-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/websiteToolboxCommunity/latest/actions/update-category', {
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
      "description": "string",
      "heading": "string",
      "isPrivate": true,
      "linked": "https://example.com",
      "locked": true,
      "object": "string",
      "parentId": 1,
      "passwordProtected": true,
      "title": "string",
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
| `linked` | string |  |
| `locked` | boolean |  |
| `object` | string |  |
| `parentId` | number |  |
| `passwordProtected` | boolean |  |
| `title` | string |  |
| `unlisted` | boolean |  |

## Native endpoint

Through the native Website Toolbox Community API, this operation is `POST /api/categories/:categoryId` (base URL `https://api.websitetoolbox.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-category.md) for the provider-specific parameters and requirements.

