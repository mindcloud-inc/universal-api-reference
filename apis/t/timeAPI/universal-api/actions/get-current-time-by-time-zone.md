# TimeAPI: Get Current Time By Time Zone

Retrieves the current time for an IANA time zone from TimeAPI.

```
GET https://connect.mindcloud.co/v1/universal/timeAPI/latest/actions/get-current-time-by-time-zone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimeAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeAPI/latest/actions/get-current-time-by-time-zone?connectionId=$CONNECTION_ID&timezone=Europe%2FAmsterdam" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "timezone": "Europe/Amsterdam"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeAPI/latest/actions/get-current-time-by-time-zone?${params}`, {
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
| `timezone` | string | yes | Full IANA time zone name, for example Europe/Amsterdam. Example: `Europe/Amsterdam`. |

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
| `date_time` | date | Current local date and time in the requested timezone. |
| `day_of_week` | string | Day of week. |
| `dst_active` | boolean | Whether daylight saving time is active. |
| `time` | string | Current local time. |
| `timezone` | string | IANA timezone name. |
| `utc_offset_seconds` | number | UTC offset in seconds. |

## Native endpoint

Through the native TimeAPI API, this operation is `GET /api/v1/time/current/zone` (base URL `https://www.timeapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-time-by-time-zone.md) for the provider-specific parameters and requirements.

