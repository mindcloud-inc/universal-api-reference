# Zenvoices Universal API Examples

These examples use the MindCloud API key and Zenvoices connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Token Login

Retrieves an access token from Zenvoices.

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

Example response:

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

See the full [Token Login action reference](actions/token-login.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zenvoices/latest/actions/token-login).
