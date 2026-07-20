# Document360: Get Article



```
GET https://connect.mindcloud.co/v1/universal/document360/latest/actions/get-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/document360/latest/actions/get-article?connectionId=$CONNECTION_ID&articleId=string&langCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "articleId": "string",
  "langCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/document360/latest/actions/get-article?${params}`, {
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
| `articleId` | string | yes |  |
| `langCode` | string | yes |  |

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
      "createdAt": "2026-05-07T12:00:00.000Z",
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
      "modifiedAt": "2026-05-07T12:00:00.000Z",
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
| `createdAt` | date |  |
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
| `modifiedAt` | date |  |
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

Through the native Document360 API, this operation is `GET /v2/Articles/:articleId/:langCode` (base URL `https://apihub.document360.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-article.md) for the provider-specific parameters and requirements.

