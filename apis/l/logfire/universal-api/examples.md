# Logfire Universal API Examples

These examples use the MindCloud API key and Logfire connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Run Query

Runs a query against Logfire data.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logfire/latest/actions/run-query?connectionId=$CONNECTION_ID&sql=SELECT%20start_timestamp%2C%20message%20FROM%20records%20LIMIT%2010" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sql": "SELECT start_timestamp, message FROM records LIMIT 10"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logfire/latest/actions/run-query?${params}`, {
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

See the full [Run Query action reference](actions/run-query.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/logfire/latest/actions/run-query).
