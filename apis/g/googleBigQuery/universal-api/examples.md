# Google BigQuery Universal API Examples

These examples use the MindCloud API key and Google BigQuery connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Query



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleBigQuery/latest/actions/query" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleBigQuery/latest/actions/query', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "query": "string"
  })
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

See the full [Query action reference](actions/query.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleBigQuery/latest/actions/query).
