# Where the ISS at: Get Coordinate Timezone



```
GET https://connect.mindcloud.co/v1/universal/whereTheISSAt/latest/actions/get-coordinate-timezone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Where the ISS at `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whereTheISSAt/latest/actions/get-coordinate-timezone?connectionId=$CONNECTION_ID&latitude=1&longitude=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "latitude": "1",
  "longitude": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whereTheISSAt/latest/actions/get-coordinate-timezone?${params}`, {
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
| `latitude` | number | yes | Latitude in decimal degrees. |
| `longitude` | number | yes | Longitude in decimal degrees. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country_code": "string",
      "latitude": "string",
      "longitude": "string",
      "map_url": "https://example.com",
      "offset": 1,
      "timezone_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country_code` | string | Country code. |
| `latitude` | string | Requested latitude. |
| `longitude` | string | Requested longitude. |
| `map_url` | string | Map URL for the coordinates. |
| `offset` | number | Current timezone offset. |
| `timezone_id` | string | IANA timezone ID. |

## Native endpoint

Through the native Where the ISS at API, this operation is `GET /coordinates/:latitude,:longitude` (base URL `https://api.wheretheiss.at/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-coordinate-timezone.md) for the provider-specific parameters and requirements.

