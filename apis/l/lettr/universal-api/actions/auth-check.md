# Lettr: Auth Check



```
GET https://connect.mindcloud.co/v1/universal/lettr/latest/actions/auth-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lettr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lettr/latest/actions/auth-check?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lettr/latest/actions/auth-check?${params}`, {
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
      "data": {
        "team_id": 1,
        "timestamp": "2026-05-07T12:00:00.000Z"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Validated team context. |
| `data.team_id` | number | The Lettr team ID associated with the API key. |
| `data.timestamp` | date | ISO 8601 timestamp for the auth check response. |
| `message` | string | Status message from Lettr. |

## Native endpoint

Through the native Lettr API, this operation is `GET /auth/check` (base URL `https://app.lettr.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/auth-check.md) for the provider-specific parameters and requirements.

