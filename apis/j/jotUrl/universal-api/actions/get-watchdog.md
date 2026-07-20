# JotUrl: Get Watchdog

Retrieves a watchdog from JotUrl.

```
GET https://connect.mindcloud.co/v1/universal/jotUrl/latest/actions/get-watchdog
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JotUrl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jotUrl/latest/actions/get-watchdog?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jotUrl/latest/actions/get-watchdog?${params}`, {
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
      "spider": "string",
      "watchdog": "string",
      "watchdog_is_default": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `spider` | string |  |
| `watchdog` | string |  |
| `watchdog_is_default` | string |  |

## Native endpoint

Through the native JotUrl API, this operation is `GET /watchdogs/info` (base URL `https://joturl.com/a/i1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-watchdog.md) for the provider-specific parameters and requirements.

