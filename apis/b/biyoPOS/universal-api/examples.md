# Biyo POS Universal API Examples

These examples use the MindCloud API key and Biyo POS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Categories

Retrieves category records from Biyo POS.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/biyoPOS/latest/actions/list-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/biyoPOS/latest/actions/list-categories?${params}`, {
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
      "active": true,
      "archived": true,
      "color": 1,
      "description": "string",
      "id": 1,
      "image": "string",
      "name": "Ava Chen",
      "parent": {},
      "sorting": 1
    }
  ],
  "meta": {}
}
```

See the full [List Categories action reference](actions/list-categories.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/biyoPOS/latest/actions/list-categories).
