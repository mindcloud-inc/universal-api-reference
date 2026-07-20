# Nutrient - Extract from PDF Universal API Examples

These examples use the MindCloud API key and Nutrient - Extract from PDF connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Convert PDF to Markdown

Converts a PDF to Markdown with Nutrient.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nutrientExtractFromPDF/latest/actions/convert-pdf-to-markdown?connectionId=$CONNECTION_ID&file=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nutrientExtractFromPDF/latest/actions/convert-pdf-to-markdown?${params}`, {
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

See the full [Convert PDF to Markdown action reference](actions/convert-pdf-to-markdown.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nutrientExtractFromPDF/latest/actions/convert-pdf-to-markdown).
