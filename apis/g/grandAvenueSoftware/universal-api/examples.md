# Grand Avenue Software Universal API Examples

These examples use the MindCloud API key and Grand Avenue Software connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Activity Log Entry

Retrieves an activity log entry from Grand Avenue Software by ID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grandAvenueSoftware/latest/actions/get-activity-log-entry?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grandAvenueSoftware/latest/actions/get-activity-log-entry?${params}`, {
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

See the full [Get Activity Log Entry action reference](actions/get-activity-log-entry.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/grandAvenueSoftware/latest/actions/get-activity-log-entry).
