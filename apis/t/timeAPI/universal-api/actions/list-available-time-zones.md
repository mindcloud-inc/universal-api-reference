# TimeAPI: List Available Time Zones

Retrieves available IANA time zones from TimeAPI.

```
GET https://connect.mindcloud.co/v1/universal/timeAPI/latest/actions/list-available-time-zones
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimeAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeAPI/latest/actions/list-available-time-zones?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeAPI/latest/actions/list-available-time-zones?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "timezones": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `timezones` | array<string> | Available IANA time zone names returned by TimeAPI. |

## Native endpoint

Through the native TimeAPI API, this operation is `GET /api/v1/timezone/availabletimezones` (base URL `https://www.timeapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-time-zones.md) for the provider-specific parameters and requirements.

