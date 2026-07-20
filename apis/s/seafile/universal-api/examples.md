# Seafile Universal API Examples

These examples use the MindCloud API key and Seafile connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Info

Retrieves the current account information from Seafile.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seafile/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seafile/latest/actions/get-account-info?${params}`, {
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
      "ai_cost": 1,
      "ai_credit": 1,
      "ai_usage_rate": "string",
      "avatar_url": "https://example.com",
      "collaborate_email_interval": 1,
      "contact_email": "ava@example.com",
      "department": "string",
      "email": "ava@example.com",
      "enable_subscription": true,
      "file_updates_email_interval": 1,
      "institution": "string",
      "is_org_staff": 1,
      "is_staff": true,
      "login_id": "string",
      "name": "Ava Chen",
      "space_usage": "string",
      "total": 1,
      "usage": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Account Info action reference](actions/get-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/seafile/latest/actions/get-account-info).
