# BASIC: Get auth token

Creates OAuth tokens in BASIC.

```
POST https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-auth-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BASIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-auth-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-auth-token', {
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
      "access_token": "string",
      "expires_in": 1,
      "id_token": "string",
      "refresh_token": "string",
      "scope": "string",
      "token_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_token` | string |  |
| `expires_in` | number |  |
| `id_token` | string |  |
| `refresh_token` | string |  |
| `scope` | string |  |
| `token_type` | string |  |

## Native endpoint

Through the native BASIC API, this operation is `POST /auth/token` (base URL `https://api.basic.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-auth-token.md) for the provider-specific parameters and requirements.

