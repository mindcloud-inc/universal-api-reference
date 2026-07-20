# Document360: Search Articles in Project Version



```
GET https://connect.mindcloud.co/v1/universal/document360/latest/actions/search-articles-in-project-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/document360/latest/actions/search-articles-in-project-version?connectionId=$CONNECTION_ID&projectVersionId=string&langCode=string&searchQuery=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectVersionId": "string",
  "langCode": "string",
  "searchQuery": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/document360/latest/actions/search-articles-in-project-version?${params}`, {
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
| `langCode` | string | yes | The language code |
| `searchQuery` | string | yes | The phrase to search for |
| `page` | number | no | Page number, zero-based |
| `hitsPerPage` | number | no | Number of hits per page |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hits": [
        {}
      ],
      "hitsPerPage": 1,
      "nbHits": 1,
      "nbPages": 1,
      "page": 1,
      "processingTimeMS": 1,
      "query": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hits` | array<object> |  |
| `hitsPerPage` | number |  |
| `nbHits` | number |  |
| `nbPages` | number |  |
| `page` | number |  |
| `processingTimeMS` | number |  |
| `query` | string |  |

## Native endpoint

Through the native Document360 API, this operation is `GET /v2/ProjectVersions/:projectVersionId/:langCode` (base URL `https://apihub.document360.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-articles-in-project-version.md) for the provider-specific parameters and requirements.

