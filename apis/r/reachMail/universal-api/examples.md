# ReachMail Universal API Examples

These examples use the MindCloud API key and ReachMail connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from ReachMail.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reachMail/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reachMail/latest/actions/get-current-user?${params}`, {
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
      "AccountId": "string",
      "AccountKey": "string",
      "CompanyName": "Ava Chen",
      "Email": "ava@example.com",
      "Name": "Ava Chen",
      "Username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/reachMail/latest/actions/get-current-user).
