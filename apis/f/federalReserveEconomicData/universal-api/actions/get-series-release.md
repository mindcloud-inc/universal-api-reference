# Federal Reserve Economic Data: Get Series Release

Retrieves the release for a series from Federal Reserve Economic Data.

```
GET https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/get-series-release
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Federal Reserve Economic Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/get-series-release?connectionId=$CONNECTION_ID&series_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "series_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/get-series-release?${params}`, {
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
| `releases[].id` | number |  |
| `releases[].link` | string |  |
| `releases[].name` | string |  |
| `releases[].notes` | string |  |
| `releases[].press_release` | boolean |  |
| `releases[].realtime_end` | date |  |
| `releases[].realtime_start` | date |  |

## Native endpoint

Through the native Federal Reserve Economic Data API, this operation is `GET /fred/series/release` (base URL `https://api.stlouisfed.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-series-release.md) for the provider-specific parameters and requirements.

