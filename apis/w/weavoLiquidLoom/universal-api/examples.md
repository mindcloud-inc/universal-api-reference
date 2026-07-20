# Weavo Liquid Loom Universal API Examples

These examples use the MindCloud API key and Weavo Liquid Loom connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## CSV to JSON

Creates JSON output from CSV in Weavo Liquid Loom.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/weavoLiquidLoom/latest/actions/csv-to-json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inputString": "Paste CSV input"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weavoLiquidLoom/latest/actions/csv-to-json', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inputString": "Paste CSV input"
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

See the full [CSV to JSON action reference](actions/csv-to-json.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/weavoLiquidLoom/latest/actions/csv-to-json).
