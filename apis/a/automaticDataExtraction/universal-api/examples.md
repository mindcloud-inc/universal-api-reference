# Automatic Data Extraction Universal API Examples

These examples use the MindCloud API key and Automatic Data Extraction connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Extract Browser HTML

Extracts browser HTML in Automatic Data Extraction.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/automaticDataExtraction/latest/actions/extract-browser-html?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/automaticDataExtraction/latest/actions/extract-browser-html?${params}`, {
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
      "browserHtml": "string",
      "statusCode": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Extract Browser HTML action reference](actions/extract-browser-html.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/automaticDataExtraction/latest/actions/extract-browser-html).
