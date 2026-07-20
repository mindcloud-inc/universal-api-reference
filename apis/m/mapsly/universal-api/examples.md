# Mapsly Universal API Examples

These examples use the MindCloud API key and Mapsly connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Upsert Record Using GET

Creates or updates a record in Mapsly using GET.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mapsly/latest/actions/upsert-record-using-get" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entity": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mapsly/latest/actions/upsert-record-using-get', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entity": "string",
    "id": "string"
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

See the full [Upsert Record Using GET action reference](actions/upsert-record-using-get.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mapsly/latest/actions/upsert-record-using-get).
