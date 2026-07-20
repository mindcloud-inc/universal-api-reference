# XSS PDF Solutions Universal API Examples

These examples use the MindCloud API key and XSS PDF Solutions connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Ask PDF With AI

Creates answers from a PDF in XSS PDF Solutions.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xSSPDFSolutions/latest/actions/ask-pdf-with-ai" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "Upload a PDF, or use the default sample PDF URL.",
  "questtext": "Ask a question about the PDF."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xSSPDFSolutions/latest/actions/ask-pdf-with-ai', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "Upload a PDF, or use the default sample PDF URL.",
    "questtext": "Ask a question about the PDF."
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
      "id": 1,
      "name": "Ava Chen",
      "output": {
        "data": {
          "result": "string"
        },
        "files": {
          "content": "string",
          "name": "Ava Chen",
          "path": "string"
        },
        "result": "string"
      },
      "status": "string",
      "steps": {
        "name": "Ava Chen",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Ask PDF With AI action reference](actions/ask-pdf-with-ai.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/xSSPDFSolutions/latest/actions/ask-pdf-with-ai).
