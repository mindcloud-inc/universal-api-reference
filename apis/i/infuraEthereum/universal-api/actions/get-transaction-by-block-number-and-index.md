# Infura Ethereum: Get Transaction By Block Number And Index

Retrieves a transaction from Infura Ethereum by block and index.

```
GET https://connect.mindcloud.co/v1/universal/infuraEthereum/latest/actions/get-transaction-by-block-number-and-index
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infura Ethereum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infuraEthereum/latest/actions/get-transaction-by-block-number-and-index?connectionId=$CONNECTION_ID&params%5B0%5D=0x17d6510&params%5B1%5D=0x0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "params[0]": "0x17d6510",
  "params[1]": "0x0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infuraEthereum/latest/actions/get-transaction-by-block-number-and-index?${params}`, {
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
| `params[0]` | string | yes | The block number as a hex quantity. Example: `0x17d6510`. |
| `params[1]` | string | yes | The transaction index within the block as a hex quantity. Example: `0x0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blockHash": "string",
      "blockNumber": "string",
      "chainId": "string",
      "from": "string",
      "gas": "string",
      "gasPrice": "string",
      "hash": "string",
      "input": "string",
      "maxFeePerGas": "string",
      "maxPriorityFeePerGas": "string",
      "nonce": "string",
      "to": "string",
      "transactionIndex": "string",
      "type": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blockHash` | string | The block hash containing the transaction. |
| `blockNumber` | string | The block number as a hex quantity. |
| `chainId` | string | The chain ID as a hex quantity. |
| `from` | string | The sender address. |
| `gas` | string | The gas limit as a hex quantity. |
| `gasPrice` | string | The gas price as a hex quantity. |
| `hash` | string | The transaction hash. |
| `input` | string | The input data payload as a hex string. |
| `maxFeePerGas` | string | The max fee per gas as a hex quantity. |
| `maxPriorityFeePerGas` | string | The max priority fee per gas as a hex quantity. |
| `nonce` | string | The sender nonce as a hex quantity. |
| `to` | string | The recipient address. |
| `transactionIndex` | string | The transaction index in the block as a hex quantity. |
| `type` | string | The transaction type as a hex quantity. |
| `value` | string | The transferred value as a hex quantity in wei. |

## Native endpoint

Through the native Infura Ethereum API, this operation is `POST /v3/:apiKey` (base URL `https://mainnet.infura.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction-by-block-number-and-index.md) for the provider-specific parameters and requirements.

