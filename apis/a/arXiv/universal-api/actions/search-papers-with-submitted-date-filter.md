# arXiv: Search Papers With Submitted Date Filter

Finds papers in arXiv by submitted date range.

```
GET https://connect.mindcloud.co/v1/universal/arXiv/latest/actions/search-papers-with-submitted-date-filter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a arXiv `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/arXiv/latest/actions/search-papers-with-submitted-date-filter?connectionId=$CONNECTION_ID&limit=25&offset=0&searchQuery=au%3Adel_maestro%20AND%20submittedDate%3A%5B202301010600%2BTO%2B202401010600%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "searchQuery": "au:del_maestro AND submittedDate:[202301010600+TO+202401010600]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/arXiv/latest/actions/search-papers-with-submitted-date-filter?${params}`, {
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
| `searchQuery` | string | yes | Required full search expression that includes the submittedDate filter, for example au:del_maestro AND submittedDate:[202301010600+TO+202401010600]. Example: `au:del_maestro AND submittedDate:[202301010600+TO+202401010600]`. |

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

Through the native arXiv API, this operation is `GET /query` (base URL `https://export.arxiv.org/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-papers-with-submitted-date-filter.md) for the provider-specific parameters and requirements.

