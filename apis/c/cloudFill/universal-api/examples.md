# CloudFill Universal API Examples

These examples use the MindCloud API key and CloudFill connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List PDFs

Retrieves available PDFs from your CloudFill account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudFill/latest/actions/list-pdfs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudFill/latest/actions/list-pdfs?${params}`, {
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
      "createdAt": 1,
      "fileName": "Ava Chen",
      "key": "string"
    }
  ],
  "meta": {}
}
```

See the full [List PDFs action reference](actions/list-pdfs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cloudFill/latest/actions/list-pdfs).

## Generate PDF

Generates a PDF from a CloudFill template.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloudFill/latest/actions/generate-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pdfKey": "pdf_abc123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudFill/latest/actions/generate-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pdfKey": "pdf_abc123"
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
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Generate PDF action reference](actions/generate-pdf.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cloudFill/latest/actions/generate-pdf).
