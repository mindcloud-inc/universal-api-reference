# Flow Blockchain: Get EVM Transaction by Hash

Retrieves an EVM transaction from Flow Blockchain by hash.

```
GET https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-evm-transaction-by-hash
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flow Blockchain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-evm-transaction-by-hash?connectionId=$CONNECTION_ID&params%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "params[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-evm-transaction-by-hash?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params[]` | array<object> | yes | Ordered JSON-RPC params array: [transaction hash]. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "jsonrpc": "string",
      "result": {}
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
| `result` | object | EVM transaction object. |

## Native endpoint

Through the native Flow Blockchain API, this operation is `POST https://mainnet.evm.nodes.onflow.org` (base URL `https://rest-mainnet.onflow.org/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-evm-transaction-by-hash.md) for the provider-specific parameters and requirements.

