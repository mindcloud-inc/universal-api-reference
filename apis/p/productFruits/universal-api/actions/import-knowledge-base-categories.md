# Product Fruits: Import Knowledge Base Categories



```
PUT https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/import-knowledge-base-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Product Fruits `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/import-knowledge-base-categories" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "categories[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/import-knowledge-base-categories', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "categories[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `categories[]` | array<object> | yes | Array of category objects to import or update. |
| `config.articleHandling` | string | no | Reserved import category handling mode; currently documented as error. |
| `config.slugConflictHandling` | string | no | How to handle slug conflicts: error or auto-number. |

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
          "status": "string",
          "title": "string"
        }
      ],
      "correlationId": "string",
      "icon": "string",
      "id": 1,
      "isFeatured": true,
      "order": 1,
      "parentCategoryId": 1,
      "status": "string"
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
| `contents[].status` | string |  |
| `contents[].title` | string |  |
| `correlationId` | string |  |
| `icon` | string |  |
| `id` | number |  |
| `isFeatured` | boolean |  |
| `order` | number |  |
| `parentCategoryId` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Product Fruits API, this operation is `POST /v1/knowledgebase/categories/import` (base URL `https://api.productfruits.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-knowledge-base-categories.md) for the provider-specific parameters and requirements.

