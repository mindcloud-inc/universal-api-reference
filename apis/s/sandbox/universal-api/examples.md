# Sandbox Universal API Examples

These examples use the MindCloud API key and Sandbox connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search GSTIN

Retrieves GST registration details from Sandbox by GSTIN.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sandbox/latest/actions/search-gstin?connectionId=$CONNECTION_ID&gstin=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "gstin": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sandbox/latest/actions/search-gstin?${params}`, {
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
      "code": 1,
      "data": {},
      "timestamp": 1,
      "transaction_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Search GSTIN action reference](actions/search-gstin.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sandbox/latest/actions/search-gstin).
