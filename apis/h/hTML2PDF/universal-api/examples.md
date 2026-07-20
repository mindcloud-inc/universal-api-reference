# HTML 2 PDF Universal API Examples

These examples use the MindCloud API key and HTML 2 PDF connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Generate PDF



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hTML2PDF/latest/actions/generate-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "html": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hTML2PDF/latest/actions/generate-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "html": "string"
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

See the full [Generate PDF action reference](actions/generate-pdf.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hTML2PDF/latest/actions/generate-pdf).
