# FraudSentinel Universal API Examples

These examples use the MindCloud API key and FraudSentinel connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get IP Risk



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fraudSentinel/latest/actions/get-ip-risk?connectionId=$CONNECTION_ID&ip=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ip": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fraudSentinel/latest/actions/get-ip-risk?${params}`, {
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
      "flag": "string",
      "geo": "string",
      "ip": "string",
      "timestamp": 1,
      "userAgent": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get IP Risk action reference](actions/get-ip-risk.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fraudSentinel/latest/actions/get-ip-risk).
