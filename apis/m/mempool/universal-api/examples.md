# Mempool Universal API Examples

These examples use the MindCloud API key and Mempool connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Address Summary

Retrieves summary details for an address from Mempool.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-address-summary?connectionId=$CONNECTION_ID&address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-address-summary?${params}`, {
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
      "address": "string",
      "chain_stats": {},
      "mempool_stats": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Address Summary action reference](actions/get-address-summary.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mempool/latest/actions/get-address-summary).
