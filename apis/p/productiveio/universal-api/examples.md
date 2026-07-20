# Productive.io Universal API Examples

These examples use the MindCloud API key and Productive.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves users from your Productive.io account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-users?${params}`, {
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
      "attributes": {
        "accountAccessExpiresAt": "string",
        "avatarUrl": "https://example.com",
        "defaultOrganizationId": 1,
        "defaultOrganizationSlug": "string",
        "email": "ava@example.com",
        "firstName": "Ava",
        "icalToken": "string",
        "intercomHash": "string",
        "lastName": "Chen",
        "locale": "string",
        "newsletterConsent": true,
        "newsletterConsentAt": "string",
        "preferences": "string",
        "ssoProvision": true,
        "sysadmin": true,
        "sysadminPermissions": [
          "string"
        ],
        "timeZone": "string",
        "twoFactorAuth": true,
        "updatedAt": "string"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/productiveio/latest/actions/list-users).
