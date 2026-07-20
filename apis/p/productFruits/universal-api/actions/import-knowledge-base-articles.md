# Product Fruits: Import Knowledge Base Articles



```
PUT https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/import-knowledge-base-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Product Fruits `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/import-knowledge-base-articles" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "articles[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/import-knowledge-base-articles', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "articles[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `articles[]` | array<object> | yes | Array of article objects to import or update. |
| `config.ignoreImportErrors` | boolean | no | Allow partial imports by ignoring non-serious errors. |
| `config.includeContentInResponse` | boolean | no | Include full content details in the import response. |
| `config.slugConflictHandling` | string | no | How to handle slug conflicts: error or auto-number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alternateSlugs": "string",
      "articleId": 1,
      "categoryId": 1,
      "contents": [
        {
          "content": "string",
          "contentId": 1,
          "correlationId": "string",
          "keywords": "string",
          "lang": "string",
          "lead": "string",
          "published": true,
          "slug": "string",
          "status": "string",
          "title": "string"
        }
      ],
      "correlationId": "string",
      "featuredOrder": 1,
      "isFeatured": true,
      "isHidden": true,
      "isPrivate": true,
      "order": 1,
      "status": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alternateSlugs` | string |  |
| `articleId` | number |  |
| `categoryId` | number |  |
| `contents[].content` | string |  |
| `contents[].contentId` | number |  |
| `contents[].correlationId` | string |  |
| `contents[].keywords` | string |  |
| `contents[].lang` | string |  |
| `contents[].lead` | string |  |
| `contents[].published` | boolean |  |
| `contents[].slug` | string |  |
| `contents[].status` | string |  |
| `contents[].title` | string |  |
| `correlationId` | string |  |
| `featuredOrder` | number |  |
| `isFeatured` | boolean |  |
| `isHidden` | boolean |  |
| `isPrivate` | boolean |  |
| `order` | number |  |
| `status` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Product Fruits API, this operation is `POST /v1/knowledgebase/import` (base URL `https://api.productfruits.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-knowledge-base-articles.md) for the provider-specific parameters and requirements.

