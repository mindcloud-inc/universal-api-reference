# DotSimple Universal API Examples

These examples use the MindCloud API key and DotSimple connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Accounts

Retrieves connected social accounts from DotSimple.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotSimple/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dotSimple/latest/actions/list-accounts?${params}`, {
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

See the full [List Accounts action reference](actions/list-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dotSimple/latest/actions/list-accounts).
