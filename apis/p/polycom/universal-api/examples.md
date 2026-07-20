# Polycom Universal API Examples

These examples use the MindCloud API key and Polycom connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Tenants

Lists Poly Lens tenants with member, device, and room totals.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/polycom/latest/actions/list-tenants?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/polycom/latest/actions/list-tenants?${params}`, {
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
      "deviceCount": 1,
      "id": "string",
      "memberCount": 1,
      "name": "Ava Chen",
      "roomData": {
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [List Tenants action reference](actions/list-tenants.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/polycom/latest/actions/list-tenants).
