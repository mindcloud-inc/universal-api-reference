# Nutrient Document Converter Universal API Examples

These examples use the MindCloud API key and Nutrient Document Converter connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Convert Markdown to PDF

Converts Markdown to PDF in Nutrient.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nutrientDocumentConverter/latest/actions/convert-markdown-to-pdf?connectionId=$CONNECTION_ID&markdown=%23%20Hello%20from%20Nutrient%5Cn%5CnThis%20PDF%20was%20generated%20from%20Markdown." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "markdown": "# Hello from Nutrient\\n\\nThis PDF was generated from Markdown."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nutrientDocumentConverter/latest/actions/convert-markdown-to-pdf?${params}`, {
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
      "contentType": "string",
      "outputFile": "string"
    }
  ],
  "meta": {}
}
```

See the full [Convert Markdown to PDF action reference](actions/convert-markdown-to-pdf.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nutrientDocumentConverter/latest/actions/convert-markdown-to-pdf).
