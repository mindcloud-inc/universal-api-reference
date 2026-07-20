# Datumbox Universal API Examples

These examples use the MindCloud API key and Datumbox connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Language Detection

Detects a document's language in Datumbox.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datumbox/latest/actions/language-detection?connectionId=$CONNECTION_ID&text=Enter%20the%20text%20to%20analyze%20for%20language%20detection." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "Enter the text to analyze for language detection."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datumbox/latest/actions/language-detection?${params}`, {
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
      "result": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Language Detection action reference](actions/language-detection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/datumbox/latest/actions/language-detection).
