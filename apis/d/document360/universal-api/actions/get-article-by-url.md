# Document360: Get Article by URL



```
GET https://connect.mindcloud.co/v1/universal/document360/latest/actions/get-article-by-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/document360/latest/actions/get-article-by-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/document360/latest/actions/get-article-by-url?${params}`, {
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
| `url` | string | yes | The relative URL of the article without the domain |
| `redirectionMode` | number | no | How the API handles redirection |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authors": [
        {}
      ],
      "availableLanguages": [
        {}
      ],
      "categoryId": "string",
      "content": "string",
      "contentType": 1,
      "createdAt": "string",
      "createdBy": "string",
      "currentWorkflowStatusId": "string",
      "description": "string",
      "hidden": true,
      "htmlContent": "string",
      "id": "string",
      "langCode": "string",
      "latestVersion": 1,
      "modifiedAt": "string",
      "order": 1,
      "projectVersionId": "string",
      "publicVersion": 1,
      "securityVisibility": 1,
      "settings": {},
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
| `availableLanguages` | array<object> |  |
| `categoryId` | string |  |
| `content` | string |  |
| `contentType` | number |  |
| `createdAt` | string |  |
| `createdBy` | string |  |
| `currentWorkflowStatusId` | string |  |
| `description` | string |  |
| `hidden` | boolean |  |
| `htmlContent` | string |  |
| `id` | string |  |
| `langCode` | string |  |
| `latestVersion` | number |  |
| `modifiedAt` | string |  |
| `order` | number |  |
| `projectVersionId` | string |  |
| `publicVersion` | number |  |
| `securityVisibility` | number |  |
| `settings` | object |  |
| `slug` | string |  |
| `status` | number |  |
| `title` | string |  |
| `translationOption` | number |  |
| `url` | string |  |
| `versionNumber` | number |  |

## Native endpoint

Through the native Document360 API, this operation is `GET /v2/Articles` (base URL `https://apihub.document360.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-article-by-url.md) for the provider-specific parameters and requirements.

