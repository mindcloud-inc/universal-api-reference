# LoginRadius: Login With Credentials

Creates a LoginRadius access token from user credentials.

```
POST https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/login-with-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoginRadius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/login-with-credentials" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "user@example.com",
  "password": "StrongPassword123!"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/login-with-credentials', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "user@example.com",
    "password": "StrongPassword123!"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email, username, or phone identifier to log in with. Example: `user@example.com`. |
| `password` | string | yes | Password for the account. Example: `StrongPassword123!`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access_token": "string",
      "expires_in": "2026-05-07T12:00:00.000Z",
      "Profile": {},
      "refresh_token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_token` | string | Access token issued for the session. |
| `expires_in` | date | Session expiry timestamp. |
| `Profile` | object | LoginRadius profile returned for the authenticated user. |
| `refresh_token` | string | Refresh token issued for the session. |

## Native endpoint

Through the native LoginRadius API, this operation is `POST /identity/v2/auth/login` (base URL `https://api.loginradius.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/login-with-credentials.md) for the provider-specific parameters and requirements.

