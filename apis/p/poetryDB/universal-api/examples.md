# PoetryDB Universal API Examples

These examples use the MindCloud API key and PoetryDB connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Poems by Author



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/poetryDB/latest/actions/get-poems-by-author?connectionId=$CONNECTION_ID&author=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "author": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/poetryDB/latest/actions/get-poems-by-author?${params}`, {
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
      "author": "string",
      "linecount": "string",
      "lines": [
        "string"
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Poems by Author action reference](actions/get-poems-by-author.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/poetryDB/latest/actions/get-poems-by-author).
