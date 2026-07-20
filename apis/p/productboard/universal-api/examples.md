# Productboard Universal API Examples

These examples use the MindCloud API key and Productboard connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List All Features

Retrieves features from your Productboard workspace.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productboard/latest/actions/list-all-features?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productboard/latest/actions/list-all-features?${params}`, {
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
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "links": {},
      "name": "Ava Chen",
      "owner": {},
      "parent": {},
      "status": {},
      "timeframe": {},
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List All Features action reference](actions/list-all-features.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/productboard/latest/actions/list-all-features).
