# Freshsales Classic Universal API Examples

These examples use the MindCloud API key and Freshsales Classic connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Owners

Retrieves owners from Freshsales Classic.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-owners?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-owners?${params}`, {
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
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "id": 1,
      "isActive": true,
      "mobileNumber": "string",
      "workNumber": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Owners action reference](actions/list-owners.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/freshsalesClassic/latest/actions/list-owners).
