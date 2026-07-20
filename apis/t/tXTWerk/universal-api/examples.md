# TXT Werk Universal API Examples

These examples use the MindCloud API key and TXT Werk connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Analyze Text

Analyzes text content in TXT Werk.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tXTWerk/latest/actions/analyze-text?connectionId=$CONNECTION_ID&text=string&services=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string",
  "services": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tXTWerk/latest/actions/analyze-text?${params}`, {
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
      "categories": [
        {
          "confidence": 1,
          "label": "string"
        }
      ],
      "language": "string",
      "tags": [
        {
          "confidence": 1,
          "term": "string"
        }
      ],
      "text": "string",
      "timestamp": 1
    }
  ],
  "meta": {}
}
```

See the full [Analyze Text action reference](actions/analyze-text.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tXTWerk/latest/actions/analyze-text).
