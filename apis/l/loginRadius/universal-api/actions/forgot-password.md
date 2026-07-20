# LoginRadius: Forgot Password

Sends a password reset request in LoginRadius.

```
PUT https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/forgot-password
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoginRadius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/forgot-password" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "loginradius-stage3-20260401162148@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/forgot-password', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "loginradius-stage3-20260401162148@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email address for password recovery. Example: `loginradius-stage3-20260401162148@example.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userName` | string | no | User name for password recovery. Example: `lrstage320260401162148`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isPosted": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isPosted` | boolean | Whether LoginRadius accepted the forgot-password request. |

## Native endpoint

Through the native LoginRadius API, this operation is `POST /identity/v2/auth/password` (base URL `https://api.loginradius.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/forgot-password.md) for the provider-specific parameters and requirements.

