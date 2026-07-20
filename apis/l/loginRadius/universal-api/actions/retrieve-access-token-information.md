# LoginRadius: Retrieve Access Token Information

Retrieves access token details from LoginRadius.

```
GET https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/retrieve-access-token-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoginRadius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/retrieve-access-token-information?connectionId=$CONNECTION_ID&accessToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accessToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/retrieve-access-token-information?${params}`, {
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
| `accessToken` | string | yes | Bearer access token to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access_token": "string",
      "isrememberme": true,
      "provider": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_token` | string | Access token value. |
| `isrememberme` | boolean | Whether the token was issued with remember-me enabled. |
| `provider` | string | Provider associated with the access token. |

## Native endpoint

Through the native LoginRadius API, this operation is `GET /identity/v2/auth/access_token` (base URL `https://api.loginradius.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-access-token-information.md) for the provider-specific parameters and requirements.

