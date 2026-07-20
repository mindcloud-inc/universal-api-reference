# GitBook: Search Site

Finds content in a GitBook site by query.

```
GET https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/search-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitBook `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/search-site?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=string&query=string&scope.mode=all&siteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationId": "string",
  "query": "string",
  "scope.mode": "all",
  "siteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/search-site?${params}`, {
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
| `organizationId` | string | yes |  |
| `query` | string | yes | Search query text. |
| `scope.mode` | string | yes | Search in all sections and site spaces, or narrow the search with a different scope mode. Default: `all`. |
| `siteId` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scope.currentSiteSpace` | string | no | Include a specific current site space when using the default search scope. |
| `scope.siteSpaceIds[]` | array<string> | no | Search only within the provided site spaces when using the specific search scope. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "pages": [
        {}
      ],
      "score": 1,
      "title": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | string |  |
| `pages` | array<object> |  |
| `score` | number |  |
| `title` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native GitBook API, this operation is `POST /orgs/:organizationId/sites/:siteId/search` (base URL `https://api.gitbook.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-site.md) for the provider-specific parameters and requirements.

