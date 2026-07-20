# Solana Universal API Examples

These examples use the MindCloud API key and Solana connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Block Height

Retrieves the current block height from Solana.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/solana/latest/actions/get-block-height?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/solana/latest/actions/get-block-height?${params}`, {
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
      "id": "string",
      "jsonrpc": "string",
      "result": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Block Height action reference](actions/get-block-height.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/solana/latest/actions/get-block-height).
