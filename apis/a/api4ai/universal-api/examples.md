# api4ai Universal API Examples

These examples use the MindCloud API key and api4ai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get OCR API Version

Retrieves the OCR API version from api4ai.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/api4ai/latest/actions/get-ocrapi-version?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/api4ai/latest/actions/get-ocrapi-version?${params}`, {
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
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get OCR API Version action reference](actions/get-ocrapi-version.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/api4ai/latest/actions/get-ocrapi-version).
