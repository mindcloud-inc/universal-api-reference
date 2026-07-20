# PDF-app Universal API Examples

These examples use the MindCloud API key and PDF-app connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Analyze File With AI

Retrieves AI analysis from a file in PDF-app.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/analyze-file-with-ai?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/analyze-file-with-ai?${params}`, {
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

See the full [Analyze File With AI action reference](actions/analyze-file-with-ai.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pDFApp/latest/actions/analyze-file-with-ai).

## Add Watermark

Updates a PDF with a watermark in PDF-app.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/add-watermark" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileUrl": "https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/add-watermark', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileUrl": "https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf"
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
      "creditsConsumed": 1,
      "creditsRemaining": 1,
      "job_id": "string",
      "message": "string",
      "presignedUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Add Watermark action reference](actions/add-watermark.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pDFApp/latest/actions/add-watermark).
