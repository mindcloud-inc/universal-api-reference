# WiseOCR Universal API Examples

These examples use the MindCloud API key and WiseOCR connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Extract Receipt Data From Text

Retrieves extracted receipt data from WiseOCR using text.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wiseOCR/latest/actions/extract-receipt-data-from-text?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wiseOCR/latest/actions/extract-receipt-data-from-text?${params}`, {
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

See the full [Extract Receipt Data From Text action reference](actions/extract-receipt-data-from-text.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wiseOCR/latest/actions/extract-receipt-data-from-text).
