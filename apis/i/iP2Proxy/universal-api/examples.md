# IP2Proxy Universal API Examples

These examples use the MindCloud API key and IP2Proxy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Proxy Lookup

Retrieves proxy details for an IP address from IP2Proxy.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iP2Proxy/latest/actions/get-proxy-lookup?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iP2Proxy/latest/actions/get-proxy-lookup?${params}`, {
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

See the full [Get Proxy Lookup action reference](actions/get-proxy-lookup.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iP2Proxy/latest/actions/get-proxy-lookup).
