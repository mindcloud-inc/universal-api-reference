# arXiv: Search Papers

Finds papers in arXiv by search query.

```
GET https://connect.mindcloud.co/v1/universal/arXiv/latest/actions/search-papers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a arXiv `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/arXiv/latest/actions/search-papers?connectionId=$CONNECTION_ID&limit=25&offset=0&searchQuery=all%3Atransformer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "searchQuery": "all:transformer"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/arXiv/latest/actions/search-papers?${params}`, {
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
| `searchQuery` | string | yes | Required arXiv search expression using the documented prefix syntax such as all:, ti:, au:, abs:, cat:, or submittedDate:[YYYYMMDDTTTT+TO+YYYYMMDDTTTT]. Example: `all:transformer`. |
| `sortBy` | list | no | Optional arXiv sort field. One of: `0`, `1`, `2`. Default: `relevance`. |
| `sortOrder` | list | no | Optional arXiv sort direction. One of: `0`, `1`. Default: `descending`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idList` | string | no | Optional comma-separated arXiv IDs. When provided with Search Query, arXiv returns only IDs that also match the query. Example: `2501.01234,hep-th/9901001`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "arxiv:comment": "string",
      "arxiv:primary_category": {},
      "author": [
        {}
      ],
      "category": [
        {}
      ],
      "id": "string",
      "published": "2026-05-07T12:00:00.000Z",
      "summary": "string",
      "title": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `arxiv:comment` | string | Optional arXiv comment field. |
| `arxiv:primary_category` | object | Primary arXiv category object. |
| `author` | array<object> | Author list objects containing author names. |
| `category` | array<object> | Category list objects from the Atom feed. |
| `id` | string | Canonical arXiv abstract URL for the paper version. |
| `published` | date | Original submission timestamp for version 1. |
| `summary` | string | Paper abstract. |
| `title` | string | Paper title. |
| `updated` | date | Last update timestamp for this paper version. |

## Native endpoint

Through the native arXiv API, this operation is `GET /query` (base URL `https://export.arxiv.org/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-papers.md) for the provider-specific parameters and requirements.

