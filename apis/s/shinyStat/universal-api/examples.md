# ShinyStat Universal API Examples

These examples use the MindCloud API key and ShinyStat connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Sign In

Retrieves an authenticated session from ShinyStat.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shinyStat/latest/actions/sign-in?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shinyStat/latest/actions/sign-in?${params}`, {
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

See the full [Sign In action reference](actions/sign-in.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shinyStat/latest/actions/sign-in).
