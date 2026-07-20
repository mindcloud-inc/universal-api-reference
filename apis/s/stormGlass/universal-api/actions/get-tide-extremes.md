# Storm Glass: Get Tide Extremes

Retrieves tide extremes from Storm Glass.

```
GET https://connect.mindcloud.co/v1/universal/stormGlass/latest/actions/get-tide-extremes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Storm Glass `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stormGlass/latest/actions/get-tide-extremes?connectionId=$CONNECTION_ID&lat=37.7749&lng=-122.4194" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lat": "37.7749",
  "lng": "-122.4194"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stormGlass/latest/actions/get-tide-extremes?${params}`, {
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
| `lat` | number | yes | Latitude of the desired tide coordinate in decimal degrees. Default: `37.7749`. |
| `lng` | number | yes | Longitude of the desired tide coordinate in decimal degrees. Default: `-122.4194`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `start` | string | no | Optional UTC start timestamp as UNIX time or URL-encoded ISO time. |
| `end` | string | no | Optional UTC end timestamp as UNIX time or URL-encoded ISO time. |
| `datum` | string | no | Optional tide datum. Use MSL or MLLW. Default: `MSL`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
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
| `data` | array<object> | High and low tide extreme records. |
| `meta` | object | Request metadata, quota, and tide station details. |

## Native endpoint

Through the native Storm Glass API, this operation is `GET /tide/extremes/point` (base URL `https://api.stormglass.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tide-extremes.md) for the provider-specific parameters and requirements.

