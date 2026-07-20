# AI Textraction Universal API Examples

These examples use the MindCloud API key and AI Textraction connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Extract Data

Extracts user-defined entities from unstructured text with AI Textraction.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aITextraction/latest/actions/extract-data?connectionId=$CONNECTION_ID&text=string&entities=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string",
  "entities": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aITextraction/latest/actions/extract-data?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Extract Data action reference](actions/extract-data.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aITextraction/latest/actions/extract-data).
