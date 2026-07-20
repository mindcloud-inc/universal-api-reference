# Precisely: Timezone By Location

Retrieves time zone details from Precisely by location.

```
GET https://connect.mindcloud.co/v1/universal/precisely/latest/actions/timezone-by-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Precisely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/precisely/latest/actions/timezone-by-location?connectionId=$CONNECTION_ID&latitude=1&longitude=1&timestamp=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "latitude": "1",
  "longitude": "1",
  "timestamp": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/precisely/latest/actions/timezone-by-location?${params}`, {
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
| `timestamp` | number | yes | Unix timestamp in milliseconds for the moment to evaluate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dstOffset": 1,
      "timestamp": 1,
      "timezoneName": "Ava Chen",
      "utcOffset": 1,
      "zoneType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dstOffset` | number | Daylight saving offset in milliseconds. |
| `timestamp` | number | Evaluated Unix timestamp in milliseconds. |
| `timezoneName` | string | Human-readable timezone name. |
| `utcOffset` | number | UTC offset in milliseconds. |
| `zoneType` | string | IANA timezone identifier. |

## Native endpoint

Through the native Precisely API, this operation is `GET /timezone/v1/timezone/bylocation` (base URL `https://api.precisely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/timezone-by-location.md) for the provider-specific parameters and requirements.

