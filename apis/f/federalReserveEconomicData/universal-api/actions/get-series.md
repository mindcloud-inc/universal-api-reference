# Federal Reserve Economic Data: Get Series

Retrieves a series from Federal Reserve Economic Data.

```
GET https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/get-series
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Federal Reserve Economic Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/get-series?connectionId=$CONNECTION_ID&series_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "series_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/get-series?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "realtime_end": "2026-05-07T12:00:00.000Z",
      "realtime_start": "2026-05-07T12:00:00.000Z",
      "seriess": [
        {
          "frequency": "string",
          "frequency_short": "string",
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `realtime_end` | date |  |
| `realtime_start` | date |  |
| `seriess[].frequency` | string |  |
| `seriess[].frequency_short` | string |  |
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

## Native endpoint

Through the native Federal Reserve Economic Data API, this operation is `GET /fred/series` (base URL `https://api.stlouisfed.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-series.md) for the provider-specific parameters and requirements.

