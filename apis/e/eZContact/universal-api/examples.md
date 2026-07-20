# EZContact Universal API Examples

These examples use the MindCloud API key and EZContact connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Contacts



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eZContact/latest/actions/search-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eZContact/latest/actions/search-contacts?${params}`, {
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

See the full [Search Contacts action reference](actions/search-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eZContact/latest/actions/search-contacts).
