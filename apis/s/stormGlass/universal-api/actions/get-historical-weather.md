# Storm Glass: Get Historical Weather

Retrieves historical weather data from Storm Glass.

```
GET https://connect.mindcloud.co/v1/universal/stormGlass/latest/actions/get-historical-weather
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Storm Glass `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stormGlass/latest/actions/get-historical-weather?connectionId=$CONNECTION_ID&lat=37.7749&lng=-122.4194&params=airTemperature%2CwindSpeed%2CwaveHeight&start=2026-04-15T00%3A00%3A00Z&end=2026-04-15T03%3A00%3A00Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lat": "37.7749",
  "lng": "-122.4194",
  "params": "airTemperature,windSpeed,waveHeight",
  "start": "2026-04-15T00:00:00Z",
  "end": "2026-04-15T03:00:00Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stormGlass/latest/actions/get-historical-weather?${params}`, {
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
| `lat` | number | yes | Latitude of the desired coordinate in decimal degrees. Default: `37.7749`. |
| `lng` | number | yes | Longitude of the desired coordinate in decimal degrees. Default: `-122.4194`. |
| `params` | string | yes | Comma-separated historical weather parameters to retrieve, such as airTemperature,windSpeed,waveHeight. Default: `airTemperature,windSpeed,waveHeight`. |
| `start` | string | yes | UTC first hour as UNIX time or ISO time. Historical requests require a start and end window. Default: `2026-04-15T00:00:00Z`. |
| `end` | string | yes | UTC final hour as UNIX time or ISO time. Each historical response covers up to 10 days. Default: `2026-04-15T03:00:00Z`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `source` | string | no | Optional source such as sg, ecmwf, ecmwf:era5, cmems, or cmems:gopaf. Default: `sg`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hours": [
        {}
      ],
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hours` | array<object> | Hourly historical weather records for the requested coordinate and time window. |
| `meta` | object | Request metadata and quota details. |

## Native endpoint

Through the native Storm Glass API, this operation is `GET /historical/point` (base URL `https://api.stormglass.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-historical-weather.md) for the provider-specific parameters and requirements.

