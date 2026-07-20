# Flow Blockchain Universal API Examples

These examples use the MindCloud API key and Flow Blockchain connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Call EVM Contract

Retrieves EVM contract call results from Flow Blockchain.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/call-evm-contract?connectionId=$CONNECTION_ID&params%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "params[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/call-evm-contract?${params}`, {
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

See the full [Call EVM Contract action reference](actions/call-evm-contract.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/flowBlockchain/latest/actions/call-evm-contract).

## Send EVM Raw Transaction

Submits a raw EVM transaction to Flow Blockchain.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/send-evm-raw-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "params[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/send-evm-raw-transaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "params[]": [{}]
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
      "id": 1,
      "jsonrpc": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

See the full [Send EVM Raw Transaction action reference](actions/send-evm-raw-transaction.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/flowBlockchain/latest/actions/send-evm-raw-transaction).
