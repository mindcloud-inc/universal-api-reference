# Text to pdf Universal API Examples

These examples use the MindCloud API key and Text to pdf connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Download File

Retrieves a file from Text to PDF by file ID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/textToPdf/latest/actions/download-file?connectionId=$CONNECTION_ID&arguments=%5Bobject%20Object%5D&arguments.fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "arguments": "[object Object]",
  "arguments.fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/textToPdf/latest/actions/download-file?${params}`, {
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
      "data": {
        "content": {
          "mimetype": "string",
          "name": "Ava Chen",
          "s3url": "https://example.com"
        }
      },
      "error": "string",
      "successful": true
    }
  ],
  "meta": {}
}
```

See the full [Download File action reference](actions/download-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/textToPdf/latest/actions/download-file).

## Convert Text to PDF

Creates a PDF document from text in Text to PDF.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/textToPdf/latest/actions/convert-text-to-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "arguments": {},
  "arguments.text": "string",
  "arguments.fileType": "txt"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/textToPdf/latest/actions/convert-text-to-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "arguments": {},
    "arguments.text": "string",
    "arguments.fileType": "txt"
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
      "data": {
        "file": {
          "mimetype": "string",
          "name": "Ava Chen",
          "s3url": "https://example.com"
        }
      },
      "error": "string",
      "successful": true
    }
  ],
  "meta": {}
}
```

See the full [Convert Text to PDF action reference](actions/convert-text-to-pdf.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/textToPdf/latest/actions/convert-text-to-pdf).
