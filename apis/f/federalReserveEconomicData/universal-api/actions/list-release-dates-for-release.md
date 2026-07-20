# Federal Reserve Economic Data: List Release Dates For Release

Retrieves release dates for a release from Federal Reserve Economic Data.

```
GET https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/list-release-dates-for-release
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Federal Reserve Economic Data `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/list-release-dates-for-release?connectionId=$CONNECTION_ID&limit=25&offset=0&release_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "release_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/list-release-dates-for-release?${params}`, {
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
| `release_id` | number | yes | The id for a release. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include_release_dates_with_no_data` | boolean | no | Return release dates even when no data is available for them. |

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
      "release_dates": [
        {
          "date": "2026-05-07T12:00:00.000Z",
          "release_id": 1
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
| `release_dates[].date` | date |  |
| `release_dates[].release_id` | number |  |
| `sort_order` | string |  |

## Native endpoint

Through the native Federal Reserve Economic Data API, this operation is `GET /fred/release/dates` (base URL `https://api.stlouisfed.org`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-release-dates-for-release.md) for the provider-specific parameters and requirements.

