# Vadivelu HTTP codes Universal API Examples

These examples use the MindCloud API key and Vadivelu HTTP codes connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get GIF Status Code Image



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vadiveluHTTPCodes/latest/actions/get-gif-status-code-image?connectionId=$CONNECTION_ID&statusCode=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "statusCode": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vadiveluHTTPCodes/latest/actions/get-gif-status-code-image?${params}`, {
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

See the full [Get GIF Status Code Image action reference](actions/get-gif-status-code-image.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vadiveluHTTPCodes/latest/actions/get-gif-status-code-image).
