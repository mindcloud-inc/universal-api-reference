# Ziflow Universal API Examples

These examples use the MindCloud API key and Ziflow connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves users from your Ziflow account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-users?${params}`, {
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
      "count": 1,
      "has_more": true,
      "page": 1,
      "users": [
        {
          "account_owner": true,
          "accounts": [
            {
              "id": "string",
              "name": "Ava Chen",
              "primary": true
            }
          ],
          "active": true,
          "api_key": "string",
          "company": "string",
          "email": "ava@example.com",
          "first_name": "Ava",
          "group": [
            "string"
          ],
          "id": "string",
          "language": "string",
          "last_name": "Chen",
          "phone": "string",
          "proofing_defaults": {
            "comment": true,
            "decision": true,
            "manage": true,
            "notification": "string",
            "share": true
          },
          "roles": [
            "string"
          ],
          "timezone": "string",
          "verified": true
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ziflow/latest/actions/list-users).
