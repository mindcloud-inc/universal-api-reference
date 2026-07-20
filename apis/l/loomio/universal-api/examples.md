# Loomio Universal API Examples

These examples use the MindCloud API key and Loomio connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Groups

Retrieves groups from Loomio.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loomio/latest/actions/list-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loomio/latest/actions/list-groups?${params}`, {
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
      "data": {},
      "meta": {},
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [List Groups action reference](actions/list-groups.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/loomio/latest/actions/list-groups).
