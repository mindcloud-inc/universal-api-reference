# Bulk24SMS Universal API Examples

These examples use the MindCloud API key and Bulk24SMS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## View Own Profile

Retrieves your user profile from Bulk24SMS.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulk24SMS/latest/actions/view-own-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulk24SMS/latest/actions/view-own-profile?${params}`, {
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

See the full [View Own Profile action reference](actions/view-own-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bulk24SMS/latest/actions/view-own-profile).
