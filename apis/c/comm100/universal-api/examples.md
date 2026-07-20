# Comm100 Universal API Examples

These examples use the MindCloud API key and Comm100 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Agent Statuses

Retrieves live chat agent statuses from Comm100.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/comm100/latest/actions/list-agent-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/comm100/latest/actions/list-agent-statuses?${params}`, {
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

See the full [List Agent Statuses action reference](actions/list-agent-statuses.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/comm100/latest/actions/list-agent-statuses).
