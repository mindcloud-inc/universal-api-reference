# Infura Ethereum: Get Block Receipts

Retrieves block receipts from Infura Ethereum.

```
GET https://connect.mindcloud.co/v1/universal/infuraEthereum/latest/actions/get-block-receipts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infura Ethereum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infuraEthereum/latest/actions/get-block-receipts?connectionId=$CONNECTION_ID&params%5B0%5D=0x17d6510" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "params[0]": "0x17d6510"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infuraEthereum/latest/actions/get-block-receipts?${params}`, {
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
| `params[0]` | string | yes | The block number or block hash to retrieve receipts for. Example: `0x17d6510`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blockHash": "string",
      "blockNumber": "string",
      "contractAddress": "string",
      "cumulativeGasUsed": "string",
      "effectiveGasPrice": "string",
      "from": "string",
      "gasUsed": "string",
      "logs": [
        {}
      ],
      "logsBloom": "string",
      "status": "string",
      "to": "string",
      "transactionHash": "string",
      "transactionIndex": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blockHash` | string | The block hash containing the receipt. |
| `blockNumber` | string | The block number as a hex quantity. |
| `contractAddress` | string | The created contract address when applicable. |
| `cumulativeGasUsed` | string | The cumulative gas used in the block as a hex quantity. |
| `effectiveGasPrice` | string | The effective gas price as a hex quantity. |
| `from` | string | The sender address. |
| `gasUsed` | string | The gas used by this transaction as a hex quantity. |
| `logs` | array<object> | The emitted log entries. |
| `logsBloom` | string | The bloom filter for the transaction logs. |
| `status` | string | The execution status as a hex quantity. |
| `to` | string | The recipient address. |
| `transactionHash` | string | The transaction hash. |
| `transactionIndex` | string | The transaction index in the block as a hex quantity. |
| `type` | string | The transaction type as a hex quantity. |

## Native endpoint

Through the native Infura Ethereum API, this operation is `POST /v3/:apiKey` (base URL `https://mainnet.infura.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-block-receipts.md) for the provider-specific parameters and requirements.

