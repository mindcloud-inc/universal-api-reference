# Document360: Get Category Page



```
GET https://connect.mindcloud.co/v1/universal/document360/latest/actions/get-category-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/document360/latest/actions/get-category-page?connectionId=$CONNECTION_ID&categoryId=string&langCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "categoryId": "string",
  "langCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/document360/latest/actions/get-category-page?${params}`, {
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
| `categoryId` | string | yes | The ID of the category |
| `langCode` | string | yes | The language code of the category |
| `isForDisplay` | boolean | no | Expand snippets and variables for display |
| `isPublished` | boolean | no | Whether to fetch the latest published category page |
| `appendSASToken` | boolean | no | Whether to append SAS tokens for images and files |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": {
        "authors": [
          {}
        ],
        "blockContent": "string",
        "content": "string",
        "contentType": "string",
        "createdAt": "string",
        "createdBy": "string",
        "currentWorkflowStatusId": "string",
        "enableRtl": true,
        "hidden": true,
        "htmlContent": "string",
        "id": "string",
        "isBlockEditor": true,
        "isFallBackContent": true,
        "latestVersion": 1,
        "modifiedAt": "string",
        "parentCategoryId": "string",
        "projectDocumentVersionId": "string",
        "publicVersion": 1,
        "slug": "string",
        "staleStatus": {},
        "status": 1,
        "title": "string",
        "versionNumber": 1
      },
      "errors": [
        {}
      ],
      "extensionData": {},
      "information": [
        {}
      ],
      "success": true,
      "warnings": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category.authors` | array<object> |  |
| `category.blockContent` | string |  |
| `category.content` | string |  |
| `category.contentType` | string |  |
| `category.createdAt` | string |  |
| `category.createdBy` | string |  |
| `category.currentWorkflowStatusId` | string |  |
| `category.enableRtl` | boolean |  |
| `category.hidden` | boolean |  |
| `category.htmlContent` | string |  |
| `category.id` | string |  |
| `category.isBlockEditor` | boolean |  |
| `category.isFallBackContent` | boolean |  |
| `category.latestVersion` | number |  |
| `category.modifiedAt` | string |  |
| `category.parentCategoryId` | string |  |
| `category.projectDocumentVersionId` | string |  |
| `category.publicVersion` | number |  |
| `category.slug` | string |  |
| `category.staleStatus` | object |  |
| `category.status` | number |  |
| `category.title` | string |  |
| `category.versionNumber` | number |  |
| `errors` | array<object> |  |
| `extensionData` | object |  |
| `information` | array<object> |  |
| `success` | boolean |  |
| `warnings` | array<object> |  |

## Native endpoint

Through the native Document360 API, this operation is `GET /v2/Categories/:categoryId/content/:langCode` (base URL `https://apihub.document360.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-category-page.md) for the provider-specific parameters and requirements.

