# Sendcrux: Generate Login Token

Creates a login token in Sendcrux.

```
POST https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/generate-login-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendcrux `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/generate-login-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/generate-login-token', {
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
      "token": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `token` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Sendcrux API, this operation is `POST /api/v1/login-token` (base URL `https://sendcrux.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-login-token.md) for the provider-specific parameters and requirements.

