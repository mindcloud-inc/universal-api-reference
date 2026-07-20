# Document360: Get Article by Version



```
GET https://connect.mindcloud.co/v1/universal/document360/latest/actions/get-article-by-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/document360/latest/actions/get-article-by-version?connectionId=$CONNECTION_ID&articleId=string&langCode=string&versionNumber=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "articleId": "string",
  "langCode": "string",
  "versionNumber": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/document360/latest/actions/get-article-by-version?${params}`, {
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
| `articleId` | string | yes | The ID of the article |
| `langCode` | string | yes | The language code of the article |
| `versionNumber` | number | yes | The version number of the article |
| `isForDisplay` | boolean | no | Expand snippets and variables for display |
| `appendSASToken` | boolean | no | Whether to append SAS tokens for images and files |

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
      "content": "string",
      "contentType": 1,
      "createdAt": "string",
      "createdBy": "string",
      "description": "string",
      "hidden": true,
      "htmlContent": "string",
      "id": "string",
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
      "versionCreatedAt": "string",
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
| `content` | string |  |
| `contentType` | number |  |
| `createdAt` | string |  |
| `createdBy` | string |  |
| `description` | string |  |
| `hidden` | boolean |  |
| `htmlContent` | string |  |
| `id` | string |  |
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
| `versionCreatedAt` | string |  |
| `versionNumber` | number |  |

## Native endpoint

Through the native Document360 API, this operation is `GET /v2/Articles/:articleId/:langCode/versions/:versionNumber` (base URL `https://apihub.document360.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-article-by-version.md) for the provider-specific parameters and requirements.

