# Where the ISS at: Get Satellite TLE



```
GET https://connect.mindcloud.co/v1/universal/whereTheISSAt/latest/actions/get-satellite-tle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Where the ISS at `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whereTheISSAt/latest/actions/get-satellite-tle?connectionId=$CONNECTION_ID&satelliteId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "satelliteId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whereTheISSAt/latest/actions/get-satellite-tle?${params}`, {
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
| `satelliteId` | number | yes | NORAD catalog ID; use 25544 for the International Space Station. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "header": "string",
      "id": "string",
      "line1": "string",
      "line2": "string",
      "name": "Ava Chen",
      "requested_timestamp": 1,
      "tle_timestamp": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `header` | string | TLE header. |
| `id` | string | Satellite ID returned by the provider. |
| `line1` | string | First TLE line. |
| `line2` | string | Second TLE line. |
| `name` | string | Satellite name. |
| `requested_timestamp` | number | Unix timestamp requested for the TLE. |
| `tle_timestamp` | number | Unix timestamp of the TLE. |

## Native endpoint

Through the native Where the ISS at API, this operation is `GET /satellites/:satelliteId/tles` (base URL `https://api.wheretheiss.at/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-satellite-tle.md) for the provider-specific parameters and requirements.

