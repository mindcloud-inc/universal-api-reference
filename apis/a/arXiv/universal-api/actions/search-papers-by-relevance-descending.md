# arXiv: Search Papers By Relevance Descending

Finds papers in arXiv by descending relevance.

```
GET https://connect.mindcloud.co/v1/universal/arXiv/latest/actions/search-papers-by-relevance-descending
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a arXiv `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/arXiv/latest/actions/search-papers-by-relevance-descending?connectionId=$CONNECTION_ID&limit=25&offset=0&searchQuery=all%3Atransformer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "searchQuery": "all:transformer"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/arXiv/latest/actions/search-papers-by-relevance-descending?${params}`, {
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
| `searchQuery` | string | yes | arXiv query string to execute. Example: `all:transformer`. |

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

Through the native arXiv API, this operation is `GET /query` (base URL `https://export.arxiv.org/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-papers-by-relevance-descending.md) for the provider-specific parameters and requirements.

