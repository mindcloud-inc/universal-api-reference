# Action1 Universal API Examples

These examples use the MindCloud API key and Action1 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User Settings

Retrieves current user settings from Action1.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/action1/latest/actions/get-current-user-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/action1/latest/actions/get-current-user-settings?${params}`, {
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
      "email": "ava@example.com",
      "emailVerified": "ava@example.com",
      "enabled": "string",
      "firstName": "Ava",
      "id": "string",
      "identityProvider": "string",
      "impersonating": "string",
      "lastName": "Chen",
      "mfa": "string",
      "phone": "string",
      "roles": "string",
      "self": "string",
      "sessionTimeout": 1,
      "system": "string",
      "systemRole": "string",
      "timezone": "string",
      "type": "string",
      "userType": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User Settings action reference](actions/get-current-user-settings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/action1/latest/actions/get-current-user-settings).
