# Edworking Universal API Examples

These examples use the MindCloud API key and Edworking connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Notifications

Retrieves notifications from Edworking, optionally filtered by project.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edworking/latest/actions/list-notifications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edworking/latest/actions/list-notifications?${params}`, {
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

See the full [List Notifications action reference](actions/list-notifications.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/edworking/latest/actions/list-notifications).
