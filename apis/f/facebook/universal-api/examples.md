# Facebook Universal API Examples

These examples use the MindCloud API key and Facebook connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Pages

List pages you manage/own

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/facebook/latest/actions/list-pages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/facebook/latest/actions/list-pages?${params}`, {
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
      "category": "string",
      "id": "string",
      "name": "Ava Chen",
      "tasks": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Pages action reference](actions/list-pages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/facebook/latest/actions/list-pages).
