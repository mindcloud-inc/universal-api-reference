# LoginRadius: MFA Login

Creates a LoginRadius access token with MFA.

```
GET https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/mfa-login
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoginRadius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/mfa-login?connectionId=$CONNECTION_ID&email=loginradius-stage3-20260401162148%40example.com&password=MindCloud!Stage3%232026" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "loginradius-stage3-20260401162148@example.com",
  "password": "MindCloud!Stage3#2026"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/mfa-login?${params}`, {
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
| `email` | string | yes | Email address used for MFA login. Example: `loginradius-stage3-20260401162148@example.com`. |
| `password` | string | yes | Password used for MFA login. Example: `MindCloud!Stage3#2026`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LoginRadius API returns.

## Native endpoint

Through the native LoginRadius API, this operation is `POST /identity/v2/auth/login/2fa` (base URL `https://api.loginradius.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mfa-login.md) for the provider-specific parameters and requirements.

