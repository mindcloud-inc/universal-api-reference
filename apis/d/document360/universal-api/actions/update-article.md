# Document360: Update Article



```
PUT https://connect.mindcloud.co/v1/universal/document360/latest/actions/update-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/document360/latest/actions/update-article" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "articleId": "string",
  "langCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/document360/latest/actions/update-article', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "articleId": "string",
    "langCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `articleId` | string | yes | The ID of the article |
| `langCode` | string | yes | The language code of the article |
| `title` | string | no | The updated title |
| `content` | string | no | The updated article content |
| `categoryId` | string | no | The destination category |
| `hidden` | boolean | no | Whether the article is hidden |
| `versionNumber` | number | no | The article version to update |
| `translationOption` | number | no | The translation status |
| `source` | string | no | Free text for reference |
| `order` | number | no | The updated position inside the category |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authors": [
        {}
      ],
      "categoryId": "string",
      "categoryType": 1,
      "content": "string",
      "contentType": 1,
      "createdAt": "string",
      "createdBy": "string",
      "currentWorkflowStatusId": "string",
      "description": "string",
      "enableRtl": true,
      "hidden": true,
      "htmlContent": "string",
      "id": "string",
      "isFallBackContent": true,
      "isSharedArticle": true,
      "latestVersion": 1,
      "modifiedAt": "string",
      "order": 1,
      "projectVersionId": "string",
      "publicVersion": 1,
      "slug": "string",
      "status": 1,
      "title": "string",
      "translationOption": 1,
      "url": "https://example.com",
      "versionNumber": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authors` | array<object> |  |
| `categoryId` | string |  |
| `categoryType` | number |  |
| `content` | string |  |
| `contentType` | number |  |
| `createdAt` | string |  |
| `createdBy` | string |  |
| `currentWorkflowStatusId` | string |  |
| `description` | string |  |
| `enableRtl` | boolean |  |
| `hidden` | boolean |  |
| `htmlContent` | string |  |
| `id` | string |  |
| `isFallBackContent` | boolean |  |
| `isSharedArticle` | boolean |  |
| `latestVersion` | number |  |
| `modifiedAt` | string |  |
| `order` | number |  |
| `projectVersionId` | string |  |
| `publicVersion` | number |  |
| `slug` | string |  |
| `status` | number |  |
| `title` | string |  |
| `translationOption` | number |  |
| `url` | string |  |
| `versionNumber` | number |  |

## Native endpoint

Through the native Document360 API, this operation is `PUT /v2/Articles/:articleId/:langCode` (base URL `https://apihub.document360.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-article.md) for the provider-specific parameters and requirements.

