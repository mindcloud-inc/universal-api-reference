# TimeAPI: Get Time Zone Details

Retrieves time zone details by IANA name from TimeAPI.

```
GET https://connect.mindcloud.co/v1/universal/timeAPI/latest/actions/get-time-zone-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimeAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeAPI/latest/actions/get-time-zone-details?connectionId=$CONNECTION_ID&timeZone=Europe%2FAmsterdam" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "timeZone": "Europe/Amsterdam"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeAPI/latest/actions/get-time-zone-details?${params}`, {
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
| `timeZone` | string | yes | Full IANA time zone name, for example Europe/Amsterdam. Example: `Europe/Amsterdam`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "current_utc_offset_seconds": 1,
      "day_of_week": "string",
      "dst_active": true,
      "dst_from": "2026-05-07T12:00:00.000Z",
      "dst_offset_seconds": 1,
      "dst_until": "2026-05-07T12:00:00.000Z",
      "dst_utc_offset_seconds": 1,
      "has_dst": true,
      "local_time": "2026-05-07T12:00:00.000Z",
      "standard_utc_offset_seconds": 1,
      "timezone": "string",
      "unix_timestamp": 1,
      "utc_time": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current_utc_offset_seconds` | number | Current UTC offset in seconds. |
| `day_of_week` | string | Current local day of week. |
| `dst_active` | boolean | Whether daylight saving time is currently active. |
| `dst_from` | date | DST start instant. |
| `dst_offset_seconds` | number | DST offset in seconds. |
| `dst_until` | date | DST end instant. |
| `dst_utc_offset_seconds` | number | Daylight saving UTC offset in seconds. |
| `has_dst` | boolean | Whether the timezone observes daylight saving time. |
| `local_time` | date | Current local time. |
| `standard_utc_offset_seconds` | number | Standard UTC offset in seconds. |
| `timezone` | string | IANA timezone name. |
| `unix_timestamp` | number | Current Unix timestamp in seconds. |
| `utc_time` | date | Current UTC time. |

## Native endpoint

Through the native TimeAPI API, this operation is `GET /api/v1/timezone/zone` (base URL `https://www.timeapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-time-zone-details.md) for the provider-specific parameters and requirements.

