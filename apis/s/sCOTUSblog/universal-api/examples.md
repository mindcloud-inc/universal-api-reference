# SCOTUSblog Universal API Examples

These examples use the MindCloud API key and SCOTUSblog connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Abbe R. Gluck Posts



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sCOTUSblog/latest/actions/list-abbe-r-gluck-posts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sCOTUSblog/latest/actions/list-abbe-r-gluck-posts?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Abbe R. Gluck Posts action reference](actions/list-abbe-r-gluck-posts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sCOTUSblog/latest/actions/list-abbe-r-gluck-posts).
