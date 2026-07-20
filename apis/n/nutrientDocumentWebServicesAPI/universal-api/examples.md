# Nutrient Document Web Services Universal API Examples

These examples use the MindCloud API key and Nutrient Document Web Services connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Analyze Build Request

Analyzes a document build request in Nutrient Document Web Services API.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nutrientDocumentWebServicesAPI/latest/actions/analyze-build-request?connectionId=$CONNECTION_ID&parts%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "parts[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nutrientDocumentWebServicesAPI/latest/actions/analyze-build-request?${params}`, {
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

See the full [Analyze Build Request action reference](actions/analyze-build-request.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nutrientDocumentWebServicesAPI/latest/actions/analyze-build-request).

## Add Watermark

Updates a document with watermarks in Nutrient Document Web Services API.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nutrientDocumentWebServicesAPI/latest/actions/add-watermark" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nutrientDocumentWebServicesAPI/latest/actions/add-watermark', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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

See the full [Add Watermark action reference](actions/add-watermark.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nutrientDocumentWebServicesAPI/latest/actions/add-watermark).
