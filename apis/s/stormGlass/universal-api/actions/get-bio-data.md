# Storm Glass: Get Bio Data

Retrieves bio data from Storm Glass.

```
GET https://connect.mindcloud.co/v1/universal/stormGlass/latest/actions/get-bio-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Storm Glass `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stormGlass/latest/actions/get-bio-data?connectionId=$CONNECTION_ID&lat=37.7749&lng=-122.4194&params=soilMoisture%2CsoilTemperature%2Csalinity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lat": "37.7749",
  "lng": "-122.4194",
  "params": "soilMoisture,soilTemperature,salinity"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stormGlass/latest/actions/get-bio-data?${params}`, {
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
| `params` | string | yes | Comma-separated bio parameters to retrieve, such as soilMoisture,soilTemperature,salinity. Default: `soilMoisture,soilTemperature,salinity`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `source` | string | no | Optional single source or comma-separated sources. Default: `sg`. |
| `start` | string | no | Optional UTC start timestamp as UNIX time or URL-encoded ISO time. |
| `end` | string | no | Optional UTC end timestamp as UNIX time or URL-encoded ISO time. |

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
| `hours` | array<object> | Hourly bio data records for the requested coordinate. |
| `meta` | object | Request metadata and quota details. |

## Native endpoint

Through the native Storm Glass API, this operation is `GET /bio/point` (base URL `https://api.stormglass.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bio-data.md) for the provider-specific parameters and requirements.

