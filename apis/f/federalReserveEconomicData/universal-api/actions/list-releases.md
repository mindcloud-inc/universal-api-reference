# Federal Reserve Economic Data: List Releases

Retrieves releases from Federal Reserve Economic Data.

```
GET https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/list-releases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Federal Reserve Economic Data `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/list-releases?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/list-releases?${params}`, {
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
      "releases": [
        {
          "id": 1,
          "link": "https://example.com",
          "name": "Ava Chen",
          "notes": "string",
          "press_release": true,
          "realtime_end": "2026-05-07T12:00:00.000Z",
          "realtime_start": "2026-05-07T12:00:00.000Z"
        }
      ],
      "sort_order": "string"
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
| `releases[].id` | number |  |
| `releases[].link` | string |  |
| `releases[].name` | string |  |
| `releases[].notes` | string |  |
| `releases[].press_release` | boolean |  |
| `releases[].realtime_end` | date |  |
| `releases[].realtime_start` | date |  |
| `sort_order` | string |  |

## Native endpoint

Through the native Federal Reserve Economic Data API, this operation is `GET /fred/releases` (base URL `https://api.stlouisfed.org`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-releases.md) for the provider-specific parameters and requirements.

