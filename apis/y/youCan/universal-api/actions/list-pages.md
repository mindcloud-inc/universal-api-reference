# YouCan: List Pages

Retrieves a list of pages from YouCan.

```
GET https://connect.mindcloud.co/v1/universal/youCan/latest/actions/list-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouCan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youCan/latest/actions/list-pages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youCan/latest/actions/list-pages?${params}`, {
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
| `limit` | string | no |  |
| `page` | string | no |  |
| `q` | string | no |  |
| `sort_field` | string | no |  |
| `sort_order` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "content": "string",
          "created_at": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "meta": {
            "description": "string",
            "images": [
              "string"
            ],
            "title": "string"
          },
          "name": "Ava Chen",
          "public_url": "https://example.com",
          "slug": "string"
        }
      ],
      "meta": {
        "pagination": {
          "count": 1,
          "current_page": 1,
          "links": {},
          "per_page": 1,
          "total": 1,
          "total_pages": 1
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].content` | string |  |
| `data[].created_at` | date |  |
| `data[].id` | string |  |
| `data[].meta` | object |  |
| `data[].meta.description` | string |  |
| `data[].meta.images` | array |  |
| `data[].meta.title` | string |  |
| `data[].name` | string |  |
| `data[].public_url` | string |  |
| `data[].slug` | string |  |
| `meta` | object |  |
| `meta.pagination` | object |  |
| `meta.pagination.count` | number |  |
| `meta.pagination.current_page` | number |  |
| `meta.pagination.links` | object |  |
| `meta.pagination.per_page` | number |  |
| `meta.pagination.total` | number |  |
| `meta.pagination.total_pages` | number |  |

## Native endpoint

Through the native YouCan API, this operation is `GET /pages` (base URL `https://api.youcan.shop`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-pages.md) for the provider-specific parameters and requirements.

