# NewsBlur: Log In

Creates a session in NewsBlur.

```
POST https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/log-in
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NewsBlur `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/log-in" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/log-in', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "authenticated": true,
      "code": 1,
      "errors": {},
      "result": "string",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authenticated` | boolean | Whether the session is authenticated. |
| `code` | number | NewsBlur result code. |
| `errors` | object | Authentication errors when login fails. |
| `result` | string | Result status. |
| `user_id` | number | Authenticated NewsBlur user ID. |

## Native endpoint

Through the native NewsBlur API, this operation is `POST /api/login` (base URL `https://www.newsblur.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/log-in.md) for the provider-specific parameters and requirements.

