# Longreads Universal API Examples

These examples use the MindCloud API key and Longreads connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Category

Retrieves a Longreads category by ID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-category?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-category?${params}`, {
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
      "description": "string",
      "id": 1,
      "link": "https://example.com",
      "name": "Ava Chen",
      "parent": 1,
      "slug": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Category action reference](actions/get-category.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/longreads/latest/actions/get-category).
