# Socialbu: Get Access Token

Creates an access token for SocialBu API requests.

```
POST https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/get-access-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socialbu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/get-access-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/get-access-token', {
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
      "expires_at": "string",
      "expires_in": 1,
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
| `expires_at` | string |  |
| `expires_in` | number |  |
| `token_type` | string |  |

## Native endpoint

Through the native Socialbu API, this operation is `POST /auth/get_token` (base URL `https://socialbu.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-access-token.md) for the provider-specific parameters and requirements.

