# PDF Tools by Tachytelic Universal API Examples

These examples use the MindCloud API key and PDF Tools by Tachytelic connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Extract PDF Pages



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFToolsByTachytelic/latest/actions/extract-pdf-pages?connectionId=$CONNECTION_ID&pdfFileContent=Base64%20PDF%20content&pageRange=1-3%2C7" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pdfFileContent": "Base64 PDF content",
  "pageRange": "1-3,7"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFToolsByTachytelic/latest/actions/extract-pdf-pages?${params}`, {
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
      "ExtractedPdf": "string"
    }
  ],
  "meta": {}
}
```

See the full [Extract PDF Pages action reference](actions/extract-pdf-pages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pDFToolsByTachytelic/latest/actions/extract-pdf-pages).
