# TikHub Universal API Examples

These examples use the MindCloud API key and TikHub connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get TikHub User Info

Retrieves the current TikHub user info.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikHub/latest/actions/get-tik-hub-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikHub/latest/actions/get-tik-hub-user-info?${params}`, {
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
      "apiKeyData": {
        "apiKeyName": "Ava Chen",
        "apiKeyScopes": [
          "string"
        ],
        "apiKeyStatus": 1,
        "createdAt": "2026-05-07T12:00:00.000Z"
      },
      "code": 1,
      "router": "string",
      "userData": {
        "accountDisabled": true,
        "balance": 1,
        "email": "ava@example.com",
        "emailVerified": true,
        "freeCredit": 1,
        "isActive": true
      }
    }
  ],
  "meta": {}
}
```

See the full [Get TikHub User Info action reference](actions/get-tik-hub-user-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tikHub/latest/actions/get-tik-hub-user-info).
