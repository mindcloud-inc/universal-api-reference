# Federal Reserve Economic Data: List Sources

Retrieves sources from Federal Reserve Economic Data.

```
GET https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/list-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Federal Reserve Economic Data `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/list-sources?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/list-sources?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "limit": 1,
      "offset": 1,
      "order_by": "string",
      "realtime_end": "2026-05-07T12:00:00.000Z",
      "realtime_start": "2026-05-07T12:00:00.000Z",
      "sort_order": "string",
      "sources": [
        {
          "id": 1,
          "link": "https://example.com",
          "name": "Ava Chen",
          "realtime_end": "2026-05-07T12:00:00.000Z",
          "realtime_start": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `limit` | number |  |
| `offset` | number |  |
| `order_by` | string |  |
| `realtime_end` | date |  |
| `realtime_start` | date |  |
| `sort_order` | string |  |
| `sources[].id` | number |  |
| `sources[].link` | string |  |
| `sources[].name` | string |  |
| `sources[].realtime_end` | date |  |
| `sources[].realtime_start` | date |  |

## Native endpoint

Through the native Federal Reserve Economic Data API, this operation is `GET /fred/sources` (base URL `https://api.stlouisfed.org`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sources.md) for the provider-specific parameters and requirements.

