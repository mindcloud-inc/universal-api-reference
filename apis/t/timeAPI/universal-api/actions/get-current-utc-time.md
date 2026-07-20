# TimeAPI: Get Current UTC Time

Retrieves the current UTC time from TimeAPI.

```
GET https://connect.mindcloud.co/v1/universal/timeAPI/latest/actions/get-current-utc-time
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimeAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeAPI/latest/actions/get-current-utc-time?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeAPI/latest/actions/get-current-utc-time?${params}`, {
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
      "utc_time": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `utc_time` | date | Current UTC timestamp returned by TimeAPI. |

## Native endpoint

Through the native TimeAPI API, this operation is `GET /api/v1/time/current/utc` (base URL `https://www.timeapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-utc-time.md) for the provider-specific parameters and requirements.

