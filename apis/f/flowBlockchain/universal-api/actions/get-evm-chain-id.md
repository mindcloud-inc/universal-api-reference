# Flow Blockchain: Get EVM Chain ID

Retrieves the EVM chain ID from Flow Blockchain.

```
GET https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-evm-chain-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flow Blockchain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-evm-chain-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-evm-chain-id?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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
| `result` | string | Flow EVM chain ID. |

## Native endpoint

Through the native Flow Blockchain API, this operation is `POST https://mainnet.evm.nodes.onflow.org` (base URL `https://rest-mainnet.onflow.org/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-evm-chain-id.md) for the provider-specific parameters and requirements.

