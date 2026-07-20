# arXiv: Filter ID List By Search Query

Finds arXiv papers from an ID list matching a query.

```
GET https://connect.mindcloud.co/v1/universal/arXiv/latest/actions/filter-id-list-by-search-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a arXiv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/arXiv/latest/actions/filter-id-list-by-search-query?connectionId=$CONNECTION_ID&searchQuery=cat%3Acs.LG&idList=2501.01234%2Chep-th%2F9901001" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searchQuery": "cat:cs.LG",
  "idList": "2501.01234,hep-th/9901001"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/arXiv/latest/actions/filter-id-list-by-search-query?${params}`, {
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
| `searchQuery` | string | yes | Full arXiv search expression used to filter the provided ID list. Example: `cat:cs.LG`. |
| `idList` | string | yes | Comma-separated arXiv paper IDs to filter. Example: `2501.01234,hep-th/9901001`. |

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

Through the native arXiv API, this operation is `GET /query` (base URL `https://export.arxiv.org/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/filter-id-list-by-search-query.md) for the provider-specific parameters and requirements.

