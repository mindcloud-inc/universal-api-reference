# Zenvoices: Token Login

Retrieves an access token from Zenvoices.

```
GET https://connect.mindcloud.co/v1/universal/zenvoices/latest/actions/token-login
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenvoices `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenvoices/latest/actions/token-login?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenvoices/latest/actions/token-login?${params}`, {
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
      "accessToken": "string",
      "accessTokenExpirationDateTimeUtc": "2026-05-07T12:00:00.000Z",
      "errorMessage": "string",
      "expireInSeconds": 1,
      "refreshToken": "string",
      "requiresTwoFactorVerification": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessToken` | string | Bearer access token returned by Zenvoices TokenLogin. |
| `accessTokenExpirationDateTimeUtc` | date | UTC access token expiration timestamp. |
| `errorMessage` | string | Error returned by Zenvoices when login cannot complete. |
| `expireInSeconds` | number | Access token lifetime in seconds. |
| `refreshToken` | string | Refresh token returned by Zenvoices TokenLogin. |
| `requiresTwoFactorVerification` | boolean | Whether the account requires two-factor verification. |

## Native endpoint

Through the native Zenvoices API, this operation is `POST /api/TokenAuth/TokenLogin` (base URL `https://app.zenvoices.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/token-login.md) for the provider-specific parameters and requirements.

