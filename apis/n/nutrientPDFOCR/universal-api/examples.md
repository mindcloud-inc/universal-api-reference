# Nutrient - PDF OCR Universal API Examples

These examples use the MindCloud API key and Nutrient - PDF OCR connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## OCR Document

Retrieves a searchable PDF from Nutrient using OCR.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nutrientPDFOCR/latest/actions/ocr-document?connectionId=$CONNECTION_ID&file=Upload%20a%20scanned%20PDF%20or%20image%20file&data.language=english" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file": "Upload a scanned PDF or image file",
  "data.language": "english"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nutrientPDFOCR/latest/actions/ocr-document?${params}`, {
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
      "pdf": "string"
    }
  ],
  "meta": {}
}
```

See the full [OCR Document action reference](actions/ocr-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nutrientPDFOCR/latest/actions/ocr-document).
