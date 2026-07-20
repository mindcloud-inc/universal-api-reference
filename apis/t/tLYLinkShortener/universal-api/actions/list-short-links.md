# TLY Link Shortener: List Short Links

Retrieves short links from TLY Link Shortener.

```
GET https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/list-short-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TLY Link Shortener `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/list-short-links?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/list-short-links?${params}`, {
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
| `search` | string | no | Search short links by text. Example: `mindcloud`. |
| `tagIds[]` | array<number> | no | Return links associated with the specified tag IDs. Example: `97527,97528`. |
| `pixelIds[]` | array<number> | no | Return links associated with the specified pixel IDs. Example: `4223`. |
| `startDate` | date | no | Filter links created on or after this date. Example: `2026-03-01T00:00:00Z`. |
| `endDate` | date | no | Filter links created on or before this date. Example: `2026-03-31T23:59:59Z`. |
| `domainIds[]` | array<number> | no | Return links associated with the specified custom domain IDs. Example: `1,2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "current_page": 1,
      "data": [
        {}
      ],
      "first_page_url": "https://example.com",
      "from": 1,
      "last_page": 1,
      "last_page_url": "https://example.com",
      "links": [
        {}
      ],
      "next_page_url": "https://example.com",
      "path": "string",
      "per_page": 1,
      "prev_page_url": "https://example.com",
      "to": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current_page` | number |  |
| `data` | array<object> |  |
| `first_page_url` | string |  |
| `from` | number |  |
| `last_page` | number |  |
| `last_page_url` | string |  |
| `links` | array<object> |  |
| `next_page_url` | string |  |
| `path` | string |  |
| `per_page` | number |  |
| `prev_page_url` | string |  |
| `to` | number |  |
| `total` | number |  |

## Native endpoint

Through the native TLY Link Shortener API, this operation is `GET /api/v1/link/list` (base URL `https://api.t.ly`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-short-links.md) for the provider-specific parameters and requirements.

