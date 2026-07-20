# Flow Blockchain: Send EVM Raw Transaction

Submits a raw EVM transaction to Flow Blockchain.

```
POST https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/send-evm-raw-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flow Blockchain `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params[]` | array<object> | yes | Ordered JSON-RPC params array: [signed raw transaction data]. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | JSON-RPC request ID. |
| `jsonrpc` | string | JSON-RPC version. |
| `result` | string | Submitted EVM transaction hash. |

## Native endpoint

Through the native Flow Blockchain API, this operation is `POST https://mainnet.evm.nodes.onflow.org` (base URL `https://rest-mainnet.onflow.org/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-evm-raw-transaction.md) for the provider-specific parameters and requirements.

