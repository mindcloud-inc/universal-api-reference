# Dandelion Universal API Examples

These examples use the MindCloud API key and Dandelion connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Detect Language From Text via HTTP GET

Retrieves detected languages from text in Dandelion via HTTP GET.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dandelion/latest/actions/detect-language-from-text-get?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dandelion/latest/actions/detect-language-from-text-get?${params}`, {
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
      "detectedLangs": [
        {}
      ],
      "time": 1,
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

See the full [Detect Language From Text via HTTP GET action reference](actions/detect-language-from-text-get.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dandelion/latest/actions/detect-language-from-text-get).
