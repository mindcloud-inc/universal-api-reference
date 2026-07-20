# HTML to PDF Universal API Examples

These examples use the MindCloud API key and HTML to PDF connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate API Key



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hTMLToPDF/latest/actions/validate-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hTMLToPDF/latest/actions/validate-api-key?${params}`, {
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
  "data": [
    {
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Validate API Key action reference](actions/validate-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hTMLToPDF/latest/actions/validate-api-key).

## Generate PDF from HTML



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hTMLToPDF/latest/actions/generate-pdf-from-html" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "html": "<html><body><h1>Hello</h1></body></html>"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hTMLToPDF/latest/actions/generate-pdf-from-html', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "html": "<html><body><h1>Hello</h1></body></html>"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Generate PDF from HTML action reference](actions/generate-pdf-from-html.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hTMLToPDF/latest/actions/generate-pdf-from-html).
