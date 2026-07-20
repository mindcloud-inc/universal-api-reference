# Product Fruits: List Knowledge Base Articles



```
GET https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/list-knowledge-base-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Product Fruits `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/list-knowledge-base-articles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/list-knowledge-base-articles?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `correlationCategoryId` | string | no | Filter articles by category correlation ID. Omit for all articles or use null for uncategorized root articles. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alternateSlugs": "string",
      "categoryId": 1,
      "contents": [
        {
          "correlationId": "string",
          "id": "string",
          "lang": "string",
          "lastModified": "2026-05-07T12:00:00.000Z",
          "published": true
        }
      ],
      "correlationId": "string",
      "featuredOrder": 1,
      "id": "string",
      "isFeatured": true,
      "isHidden": true,
      "isPrivate": true,
      "lastModified": "2026-05-07T12:00:00.000Z",
      "order": 1,
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
| `categoryId` | number |  |
| `contents[].correlationId` | string |  |
| `contents[].id` | string |  |
| `contents[].lang` | string |  |
| `contents[].lastModified` | date |  |
| `contents[].published` | boolean |  |
| `correlationId` | string |  |
| `featuredOrder` | number |  |
| `id` | string |  |
| `isFeatured` | boolean |  |
| `isHidden` | boolean |  |
| `isPrivate` | boolean |  |
| `lastModified` | date |  |
| `order` | number |  |
| `version` | string |  |

## Native endpoint

Through the native Product Fruits API, this operation is `GET /v1/knowledgebase/articles` (base URL `https://api.productfruits.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-knowledge-base-articles.md) for the provider-specific parameters and requirements.

