# AppFollow Universal API Examples

These examples use the MindCloud API key and AppFollow connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List App Collections

Retrieves app collections from AppFollow.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appFollow/latest/actions/list-app-collections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appFollow/latest/actions/list-app-collections?${params}`, {
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

See the full [List App Collections action reference](actions/list-app-collections.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/appFollow/latest/actions/list-app-collections).
