# TimeAPI: Get Current Time By IP Address

Retrieves the current time by IP address from TimeAPI.

```
GET https://connect.mindcloud.co/v1/universal/timeAPI/latest/actions/get-current-time-by-ip-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimeAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeAPI/latest/actions/get-current-time-by-ip-address?connectionId=$CONNECTION_ID&ipAddress=8.8.8.8" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ipAddress": "8.8.8.8"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeAPI/latest/actions/get-current-time-by-ip-address?${params}`, {
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
| `ipAddress` | string | yes | IPv4 address, for example 8.8.8.8. Example: `8.8.8.8`. |

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
| `date_time` | date | Current local date and time for the IP address timezone. |
| `day_of_week` | string | Day of week. |
| `dst_active` | boolean | Whether daylight saving time is active. |
| `time` | string | Current local time. |
| `timezone` | string | Resolved IANA timezone. |
| `utc_offset_seconds` | number | UTC offset in seconds. |

## Native endpoint

Through the native TimeAPI API, this operation is `GET /api/v1/time/current/ip` (base URL `https://www.timeapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-time-by-ip-address.md) for the provider-specific parameters and requirements.

