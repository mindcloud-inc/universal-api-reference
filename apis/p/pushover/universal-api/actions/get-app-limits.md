# Pushover: Get App Limits



```
GET https://connect.mindcloud.co/v1/universal/pushover/latest/actions/get-app-limits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushover `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pushover/latest/actions/get-app-limits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushover/latest/actions/get-app-limits?${params}`, {
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
      "limit": 1,
      "remaining": 1,
      "request": "string",
      "reset": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `limit` | number | Monthly message quota for the application. |
| `remaining` | number | Messages remaining in the current monthly quota window. |
| `request` | string | Pushover request identifier. |
| `reset` | number | Unix timestamp for when the monthly quota resets. |
| `status` | number | API status. Returns 1 when the limits request succeeds. |

## Native endpoint

Through the native Pushover API, this operation is `GET /apps/limits.json` (base URL `https://api.pushover.net/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-app-limits.md) for the provider-specific parameters and requirements.

