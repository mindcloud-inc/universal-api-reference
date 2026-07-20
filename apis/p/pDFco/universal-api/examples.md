# PDF.co Universal API Examples

These examples use the MindCloud API key and PDF.co connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Background Job Status

Retrieves a background job status from PDF.co.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/check-background-job-status?connectionId=$CONNECTION_ID&jobid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/check-background-job-status?${params}`, {
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
      "credits": 1,
      "duration": 1,
      "jobDuration": 1,
      "jobId": "string",
      "message": "string",
      "outputLinkValidTill": "https://example.com",
      "pageCount": 1,
      "remainingCredits": 1,
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Check Background Job Status action reference](actions/check-background-job-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pDFco/latest/actions/check-background-job-status).

## Add Content to PDF

Adds content to a PDF in PDF.co.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/add-content-to-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://pdfco-test-files.s3.us-west-2.amazonaws.com/pdf/sample.pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/add-content-to-pdf', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://pdfco-test-files.s3.us-west-2.amazonaws.com/pdf/sample.pdf"
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
      "credits": 1,
      "duration": 1,
      "error": true,
      "hash": "string",
      "name": "Ava Chen",
      "outputLinkValidTill": "https://example.com",
      "pageCount": 1,
      "remainingCredits": 1,
      "status": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Add Content to PDF action reference](actions/add-content-to-pdf.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pDFco/latest/actions/add-content-to-pdf).
