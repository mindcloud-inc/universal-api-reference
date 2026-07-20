# Olvy Universal API Examples

These examples use the MindCloud API key and Olvy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Query

Makes an authenticated raw API request to Olvy.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/olvy/latest/actions/query?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/olvy/latest/actions/query?${params}`, {
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

See the full [Query action reference](actions/query.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/olvy/latest/actions/query).
