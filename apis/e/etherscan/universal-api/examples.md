# Etherscan Universal API Examples

These examples use the MindCloud API key and Etherscan connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## eth_blockNumber

Retrieves the latest block number from Etherscan.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/etherscan/latest/actions/eth-block-number?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/etherscan/latest/actions/eth-block-number?${params}`, {
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
      "id": 1,
      "jsonrpc": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

See the full [eth_blockNumber action reference](actions/eth-block-number.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/etherscan/latest/actions/eth-block-number).
