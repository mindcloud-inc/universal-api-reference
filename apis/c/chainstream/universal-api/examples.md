# Chainstream Universal API Examples

These examples use the MindCloud API key and Chainstream connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Blockchains

Retrieves supported blockchains from Chainstream.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/list-blockchains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/list-blockchains?${params}`, {
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
      "chainId": 1,
      "explorerUrl": "https://example.com",
      "name": "Ava Chen",
      "symbol": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Blockchains action reference](actions/list-blockchains.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chainstream/latest/actions/list-blockchains).

## Calculate Wallet PnL

Calculates wallet token PnL in Chainstream.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/calculate-wallet-pnl" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chain": "string",
  "walletAddress": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/calculate-wallet-pnl', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chain": "string",
    "walletAddress": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Calculate Wallet PnL action reference](actions/calculate-wallet-pnl.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chainstream/latest/actions/calculate-wallet-pnl).
