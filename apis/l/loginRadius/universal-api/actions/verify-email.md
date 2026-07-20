# LoginRadius: Verify Email

Verifies an email address in LoginRadius.

```
PUT https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/verify-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoginRadius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/verify-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "loginradius-stage3-20260401162148@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/verify-email', {
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
| `email` | string | yes | Email address being verified. Example: `loginradius-stage3-20260401162148@example.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `otp` | string | no | Email verification OTP. Example: `123456`. |
| `verificationToken` | string | no | Email verification token. Example: `verification-token`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LoginRadius API returns.

## Native endpoint

Through the native LoginRadius API, this operation is `PUT /identity/v2/auth/email` (base URL `https://api.loginradius.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email.md) for the provider-specific parameters and requirements.

