# arXiv: Search Papers By Identifier

Finds papers in arXiv by identifier.

```
GET https://connect.mindcloud.co/v1/universal/arXiv/latest/actions/search-papers-by-identifier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a arXiv `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/arXiv/latest/actions/search-papers-by-identifier?connectionId=$CONNECTION_ID&limit=25&offset=0&searchQuery=id%3A2201.00978" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "searchQuery": "id:2201.00978"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/arXiv/latest/actions/search-papers-by-identifier?${params}`, {
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
| `searchQuery` | string | yes | Identifier search expression using the id: prefix. Example: `id:2201.00978`. |

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
| `arxiv:comment` | string |  |
| `arxiv:primary_category` | object |  |
| `author` | array<object> |  |
| `category` | array<object> |  |
| `id` | string |  |
| `published` | date |  |
| `summary` | string |  |
| `title` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native arXiv API, this operation is `GET /query` (base URL `https://export.arxiv.org/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-papers-by-identifier.md) for the provider-specific parameters and requirements.

