# Formcrafts Universal API Examples

These examples use the MindCloud API key and Formcrafts connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Workspaces

Retrieves a list of workspaces from Formcrafts.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formcrafts/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formcrafts/latest/actions/list-workspaces?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Workspaces action reference](actions/list-workspaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/formcrafts/latest/actions/list-workspaces).
