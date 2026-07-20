# Etherscan: eth_getTransactionByHash

Retrieves a transaction by hash from Etherscan.

```
GET https://connect.mindcloud.co/v1/universal/etherscan/latest/actions/eth-get-transaction-by-hash
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Etherscan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/etherscan/latest/actions/eth-get-transaction-by-hash?connectionId=$CONNECTION_ID&transactionHash=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionHash": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/etherscan/latest/actions/eth-get-transaction-by-hash?${params}`, {
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
| `chainId` | string | no | Default: `1`. |
| `transactionHash` | string | yes |  |

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
| `id` | number | JSON-RPC response id. |
| `jsonrpc` | string | JSON-RPC version. |
| `result` | object | Transaction payload returned by Etherscan. |

## Native endpoint

Through the native Etherscan API, this operation is `GET /v2/api` (base URL `https://api.etherscan.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/eth-get-transaction-by-hash.md) for the provider-specific parameters and requirements.

