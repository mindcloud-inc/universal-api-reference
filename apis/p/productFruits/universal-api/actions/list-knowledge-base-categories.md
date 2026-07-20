# Product Fruits: List Knowledge Base Categories



```
GET https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/list-knowledge-base-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Product Fruits `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/list-knowledge-base-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/list-knowledge-base-categories?${params}`, {
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
      "contents": [
        {
          "description": "string",
          "lang": "string",
          "slug": "string",
          "slug_state": "string",
          "title": "string"
        }
      ],
      "correlationId": "string",
      "icon": "string",
      "id": 1,
      "isFeatured": true,
      "order": 1,
      "parentCategoryId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contents[].description` | string |  |
| `contents[].lang` | string |  |
| `contents[].slug` | string |  |
| `contents[].slug_state` | string |  |
| `contents[].title` | string |  |
| `correlationId` | string |  |
| `icon` | string |  |
| `id` | number |  |
| `isFeatured` | boolean |  |
| `order` | number |  |
| `parentCategoryId` | number |  |

## Native endpoint

Through the native Product Fruits API, this operation is `GET /v1/knowledgebase/categories` (base URL `https://api.productfruits.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-knowledge-base-categories.md) for the provider-specific parameters and requirements.

