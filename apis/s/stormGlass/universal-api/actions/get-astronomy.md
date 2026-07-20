# Storm Glass: Get Astronomy

Retrieves astronomy data from Storm Glass.

```
GET https://connect.mindcloud.co/v1/universal/stormGlass/latest/actions/get-astronomy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Storm Glass `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stormGlass/latest/actions/get-astronomy?connectionId=$CONNECTION_ID&lat=37.7749&lng=-122.4194" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lat": "37.7749",
  "lng": "-122.4194"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stormGlass/latest/actions/get-astronomy?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `start` | string | no | Optional UTC start timestamp as UNIX time or URL-encoded ISO time. |
| `end` | string | no | Optional UTC end date or timestamp. Storm Glass returns astronomy data for up to 10 days. |

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
| `data` | array<object> | Daily astronomy records for the requested coordinate. |
| `meta` | object | Request metadata and quota details. |

## Native endpoint

Through the native Storm Glass API, this operation is `GET /astronomy/point` (base URL `https://api.stormglass.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-astronomy.md) for the provider-specific parameters and requirements.

