# Waze Deep Links Universal API Examples

These examples use the MindCloud API key and Waze Deep Links connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Address

Generates a Waze deep link URL to search an address.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wazeDeepLinks/latest/actions/search-address?connectionId=$CONNECTION_ID&q=66%20Acacia%20Avenue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "66 Acacia Avenue"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wazeDeepLinks/latest/actions/search-address?${params}`, {
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
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Search Address action reference](actions/search-address.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wazeDeepLinks/latest/actions/search-address).
