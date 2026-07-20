# Document360: Update Category Page Content



```
PUT https://connect.mindcloud.co/v1/universal/document360/latest/actions/update-category-page-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/document360/latest/actions/update-category-page-content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "categoryId": "string",
  "langCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/document360/latest/actions/update-category-page-content', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "categoryId": "string",
    "langCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `categoryId` | string | yes | The ID of the category |
| `langCode` | string | yes | Language code of the category |
| `title` | string | no | Updated category page title |
| `content` | string | no | Updated category page content |
| `versionNumber` | number | no | Specific version number to update |
| `translationOption` | string | no | Translation status override |
| `source` | string | no | Free text source reference |
| `updatedBy` | string | no | Team account ID responsible for the update |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authors": [
        {}
      ],
      "blockContent": "string",
      "categoryId": "string",
      "content": "string",
      "createdAt": "string",
      "createdBy": "string",
      "enableRtl": true,
      "hidden": true,
      "htmlContent": "string",
      "id": "string",
      "isFallBackContent": true,
      "latestVersion": 1,
      "modifiedAt": "string",
      "order": 1,
      "projectVersionId": "string",
      "publicVersion": 1,
      "slug": "string",
      "status": 1,
      "title": "string",
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
| `blockContent` | string |  |
| `categoryId` | string |  |
| `content` | string |  |
| `createdAt` | string |  |
| `createdBy` | string |  |
| `enableRtl` | boolean |  |
| `hidden` | boolean |  |
| `htmlContent` | string |  |
| `id` | string |  |
| `isFallBackContent` | boolean |  |
| `latestVersion` | number |  |
| `modifiedAt` | string |  |
| `order` | number |  |
| `projectVersionId` | string |  |
| `publicVersion` | number |  |
| `slug` | string |  |
| `status` | number |  |
| `title` | string |  |
| `versionNumber` | number |  |

## Native endpoint

Through the native Document360 API, this operation is `PUT /v2/Categories/:categoryId/content/:langCode` (base URL `https://apihub.document360.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-category-page-content.md) for the provider-specific parameters and requirements.

