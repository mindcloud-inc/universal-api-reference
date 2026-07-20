# Whop Universal API Examples

These examples use the MindCloud API key and Whop connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Members

Retrieves members from Whop for a company.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whop/latest/actions/list-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whop/latest/actions/list-members?${params}`, {
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
      "accessLevel": "string",
      "companyTokenBalance": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "joinedAt": "2026-05-07T12:00:00.000Z",
      "mostRecentAction": "string",
      "mostRecentActionAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "usdTotalSpent": 1,
      "user": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen",
        "username": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

See the full [List Members action reference](actions/list-members.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/whop/latest/actions/list-members).
