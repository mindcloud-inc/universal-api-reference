# TimeAPI: Get Current Time By Coordinates

Retrieves the current time by coordinates from TimeAPI.

```
GET https://connect.mindcloud.co/v1/universal/timeAPI/latest/actions/get-current-time-by-coordinates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimeAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeAPI/latest/actions/get-current-time-by-coordinates?connectionId=$CONNECTION_ID&latitude=38.9&longitude=-77.03" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "latitude": "38.9",
  "longitude": "-77.03"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeAPI/latest/actions/get-current-time-by-coordinates?${params}`, {
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
| `latitude` | number | yes | Latitude ranging from -90 to 90. Example: `38.9`. |
| `longitude` | number | yes | Longitude ranging from -180 to 180. Example: `-77.03`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "date_time": "2026-05-07T12:00:00.000Z",
      "day_of_week": "string",
      "dst_active": true,
      "time": "string",
      "timezone": "string",
      "utc_offset_seconds": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | Current local date. |
| `date_time` | date | Current local date and time for the coordinates. |
| `day_of_week` | string | Day of week. |
| `dst_active` | boolean | Whether daylight saving time is active. |
| `time` | string | Current local time. |
| `timezone` | string | Resolved IANA timezone. |
| `utc_offset_seconds` | number | UTC offset in seconds. |

## Native endpoint

Through the native TimeAPI API, this operation is `GET /api/v1/time/current/coordinate` (base URL `https://www.timeapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-time-by-coordinates.md) for the provider-specific parameters and requirements.

