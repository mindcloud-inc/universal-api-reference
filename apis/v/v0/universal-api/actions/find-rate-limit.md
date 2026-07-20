# v0: Find Rate Limit

Retrieves rate limit details from v0.

```
GET https://connect.mindcloud.co/v1/universal/v0/latest/actions/find-rate-limit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a v0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/v0/latest/actions/find-rate-limit?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/v0/latest/actions/find-rate-limit?${params}`, {
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
| `scope` | string | no | The scope to inspect for rate limit information. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dailyLimit": {
        "isWithinGracePeriod": true,
        "limit": 1,
        "remaining": 1,
        "reset": 1
      },
      "limit": 1,
      "remaining": 1,
      "reset": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dailyLimit.isWithinGracePeriod` | boolean |  |
| `dailyLimit.limit` | number |  |
| `dailyLimit.remaining` | number |  |
| `dailyLimit.reset` | number |  |
| `limit` | number |  |
| `remaining` | number |  |
| `reset` | number |  |

## Native endpoint

Through the native v0 API, this operation is `GET /v1/rate-limits` (base URL `https://api.v0.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-rate-limit.md) for the provider-specific parameters and requirements.

