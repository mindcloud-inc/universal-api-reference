# Document360: List Articles in Project Version



```
GET https://connect.mindcloud.co/v1/universal/document360/latest/actions/list-articles-in-project-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/document360/latest/actions/list-articles-in-project-version?connectionId=$CONNECTION_ID&projectVersionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectVersionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/document360/latest/actions/list-articles-in-project-version?${params}`, {
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
| `projectVersionId` | string | yes | The project version ID |
| `langCode` | string | no | Optional language code for filtering articles by language |
| `page` | number | no | Page number, zero-based |
| `hitsPerPage` | number | no | Number of results per page |
| `securityVisibility` | number | no | Optional protection level filter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": 1,
      "currentWorkflowStatusId": "string",
      "excludeFromExternalSearch": true,
      "hidden": true,
      "id": "string",
      "isSharedArticle": true,
      "languageCode": "string",
      "latestVersion": 1,
      "modifiedAt": "string",
      "order": 1,
      "publicVersion": 1,
      "securityVisibility": 1,
      "slug": "string",
      "status": 1,
      "title": "string",
      "translationOption": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | number |  |
| `currentWorkflowStatusId` | string |  |
| `excludeFromExternalSearch` | boolean |  |
| `hidden` | boolean |  |
| `id` | string |  |
| `isSharedArticle` | boolean |  |
| `languageCode` | string |  |
| `latestVersion` | number |  |
| `modifiedAt` | string |  |
| `order` | number |  |
| `publicVersion` | number |  |
| `securityVisibility` | number |  |
| `slug` | string |  |
| `status` | number |  |
| `title` | string |  |
| `translationOption` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Document360 API, this operation is `GET /v2/ProjectVersions/:projectVersionId/articles` (base URL `https://apihub.document360.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-articles-in-project-version.md) for the provider-specific parameters and requirements.

