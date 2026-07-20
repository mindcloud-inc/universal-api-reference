# Federal Reserve Economic Data: List Series Observations

Retrieves series observations from Federal Reserve Economic Data.

```
GET https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/list-series-observations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Federal Reserve Economic Data `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/list-series-observations?connectionId=$CONNECTION_ID&limit=25&offset=0&series_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "series_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/list-series-observations?${params}`, {
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
| `series_id` | string | yes | The id for a series. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `aggregation_method` | string | no | The aggregation method used for frequency aggregation. |
| `frequency` | string | no | Aggregate values to a lower frequency. |
| `observation_end` | date | no | The end of the observation period. |
| `observation_start` | date | no | The start of the observation period. |
| `output_type` | number | no | An integer that indicates an output type. |
| `units` | string | no | A key that indicates a data value transformation. |
| `vintage_dates` | string | no | A comma separated list of vintage dates in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "file_type": "string",
      "limit": 1,
      "observation_end": "2026-05-07T12:00:00.000Z",
      "observation_start": "2026-05-07T12:00:00.000Z",
      "observations": [
        {
          "date": "2026-05-07T12:00:00.000Z",
          "realtime_end": "2026-05-07T12:00:00.000Z",
          "realtime_start": "2026-05-07T12:00:00.000Z",
          "value": "string"
        }
      ],
      "offset": 1,
      "order_by": "string",
      "output_type": 1,
      "realtime_end": "2026-05-07T12:00:00.000Z",
      "realtime_start": "2026-05-07T12:00:00.000Z",
      "sort_order": "string",
      "units": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `file_type` | string |  |
| `limit` | number |  |
| `observation_end` | date |  |
| `observation_start` | date |  |
| `observations[].date` | date |  |
| `observations[].realtime_end` | date |  |
| `observations[].realtime_start` | date |  |
| `observations[].value` | string |  |
| `offset` | number |  |
| `order_by` | string |  |
| `output_type` | number |  |
| `realtime_end` | date |  |
| `realtime_start` | date |  |
| `sort_order` | string |  |
| `units` | string |  |

## Native endpoint

Through the native Federal Reserve Economic Data API, this operation is `GET /fred/series/observations` (base URL `https://api.stlouisfed.org`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-series-observations.md) for the provider-specific parameters and requirements.

