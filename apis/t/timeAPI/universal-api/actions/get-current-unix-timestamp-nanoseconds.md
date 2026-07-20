# TimeAPI: Get Current Unix Timestamp Nanoseconds

Retrieves the current Unix timestamp in nanoseconds from TimeAPI.

```
GET https://connect.mindcloud.co/v1/universal/timeAPI/latest/actions/get-current-unix-timestamp-nanoseconds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimeAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeAPI/latest/actions/get-current-unix-timestamp-nanoseconds?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeAPI/latest/actions/get-current-unix-timestamp-nanoseconds?${params}`, {
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
      "unix_timestamp": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `unix_timestamp` | number | Current Unix timestamp in nanoseconds. |

## Native endpoint

Through the native TimeAPI API, this operation is `GET /api/v1/time/current/unix_ns` (base URL `https://www.timeapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-unix-timestamp-nanoseconds.md) for the provider-specific parameters and requirements.

