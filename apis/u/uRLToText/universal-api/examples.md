# URL to Text Universal API Examples

These examples use the MindCloud API key and URL to Text connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Convert URL to Text

Retrieves extracted webpage or YouTube content from URL to Text.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uRLToText/latest/actions/convert-url-to-text?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uRLToText/latest/actions/convert-url-to-text?${params}`, {
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
      "content": "string",
      "creditsUsed": 1,
      "ogDescription": "string",
      "ogImageUrl": "https://example.com",
      "outputFormat": "string",
      "pageTitle": "string",
      "publishedDate": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "warning": "string"
    }
  ],
  "meta": {}
}
```

See the full [Convert URL to Text action reference](actions/convert-url-to-text.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uRLToText/latest/actions/convert-url-to-text).
