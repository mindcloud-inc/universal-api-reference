# Botsonic: List Bot Data

Retrieves bot data from Botsonic.

```
GET https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/list-bot-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botsonic `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/list-bot-data?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/list-bot-data?${params}`, {
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
| `searchQuery` | string | no | Search for bot data matching a query. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sortBy` | string | no | Bot data attribute to sort by. |
| `sortOrder` | string | no | Sort direction for bot data results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filter_by": [
        "string"
      ],
      "items": [
        {}
      ],
      "num_timed_out": 1,
      "page": 1,
      "pages": 1,
      "search_value": "string",
      "sitemap_root_url": "https://example.com",
      "size": 1,
      "sort_by": "string",
      "sort_order": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filter_by` | array<string> | Applied filters. |
| `items` | array<object> | Bot data records. |
| `num_timed_out` | number | Number of timed-out records. |
| `page` | number | Current page. |
| `pages` | number | Total pages. |
| `search_value` | string | Search value. |
| `sitemap_root_url` | string | Sitemap root URL. |
| `size` | number | Page size. |
| `sort_by` | string | Sort field. |
| `sort_order` | string | Sort direction. |
| `total` | number | Total bot data records. |

## Native endpoint

Through the native Botsonic API, this operation is `GET /v1/business/bot-data/all` (base URL `https://api.botsonic.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-bot-data.md) for the provider-specific parameters and requirements.

