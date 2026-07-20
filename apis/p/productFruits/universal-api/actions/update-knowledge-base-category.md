# Product Fruits: Update Knowledge Base Category



```
PUT https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/update-knowledge-base-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Product Fruits `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/update-knowledge-base-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "correlationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/update-knowledge-base-category', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "correlationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contents[]` | array<object> | no | Array of localized category content objects. |
| `correlationId` | string | yes | The correlation ID of the category to update. |
| `icon` | string | no | Category icon or CDN image GUID. |
| `isFeatured` | boolean | no | Whether the category is featured. |
| `order` | number | no | Display order within the parent category. |
| `parentCategoryId` | number | no | Parent category ID. Use null for a root category. |

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

Through the native Product Fruits API, this operation is `PUT /v1/knowledgebase/categories/:correlationId` (base URL `https://api.productfruits.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-knowledge-base-category.md) for the provider-specific parameters and requirements.

