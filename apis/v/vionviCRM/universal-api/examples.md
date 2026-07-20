# vionvi CRM Universal API Examples

These examples use the MindCloud API key and vionvi CRM connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Show Current User

Retrieves the current user from vionvi CRM.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vionviCRM/latest/actions/show-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vionviCRM/latest/actions/show-current-user?${params}`, {
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
      "dtDelete": 1,
      "email": "ava@example.com",
      "id": 1,
      "isActive": 1,
      "langLocale": "string",
      "name": "Ava Chen",
      "phone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Show Current User action reference](actions/show-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vionviCRM/latest/actions/show-current-user).
