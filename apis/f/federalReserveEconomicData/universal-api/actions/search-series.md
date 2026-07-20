# Federal Reserve Economic Data: Search Series

Finds series in Federal Reserve Economic Data by search text.

```
GET https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/search-series
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Federal Reserve Economic Data `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/search-series?connectionId=$CONNECTION_ID&limit=25&offset=0&search_text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "search_text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/search-series?${params}`, {
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
| `search_text` | string | yes | The words to match against economic data series. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `search_type` | string | no | Determines the type of search to perform. |

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
      "seriess": [
        {
          "frequency": "string",
          "frequency_short": "string",
          "group_popularity": 1,
          "id": "string",
          "last_updated": "string",
          "notes": "string",
          "observation_end": "2026-05-07T12:00:00.000Z",
          "observation_start": "2026-05-07T12:00:00.000Z",
          "popularity": 1,
          "realtime_end": "2026-05-07T12:00:00.000Z",
          "realtime_start": "2026-05-07T12:00:00.000Z",
          "seasonal_adjustment": "string",
          "seasonal_adjustment_short": "string",
          "title": "string",
          "units": "string",
          "units_short": "string"
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
| `seriess[].frequency` | string |  |
| `seriess[].frequency_short` | string |  |
| `seriess[].group_popularity` | number |  |
| `seriess[].id` | string |  |
| `seriess[].last_updated` | string |  |
| `seriess[].notes` | string |  |
| `seriess[].observation_end` | date |  |
| `seriess[].observation_start` | date |  |
| `seriess[].popularity` | number |  |
| `seriess[].realtime_end` | date |  |
| `seriess[].realtime_start` | date |  |
| `seriess[].seasonal_adjustment` | string |  |
| `seriess[].seasonal_adjustment_short` | string |  |
| `seriess[].title` | string |  |
| `seriess[].units` | string |  |
| `seriess[].units_short` | string |  |
| `sort_order` | string |  |

## Native endpoint

Through the native Federal Reserve Economic Data API, this operation is `GET /fred/series/search` (base URL `https://api.stlouisfed.org`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-series.md) for the provider-specific parameters and requirements.

