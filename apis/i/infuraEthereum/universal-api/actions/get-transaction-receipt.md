# Infura Ethereum: Get Transaction Receipt

Retrieves a transaction receipt from Infura Ethereum.

```
GET https://connect.mindcloud.co/v1/universal/infuraEthereum/latest/actions/get-transaction-receipt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infura Ethereum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infuraEthereum/latest/actions/get-transaction-receipt?connectionId=$CONNECTION_ID&params%5B0%5D=0x714d09606652a43a4f47cf7f59b88659bdf54a4fa7eeb34a307fbc3671b46340" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "params[0]": "0x714d09606652a43a4f47cf7f59b88659bdf54a4fa7eeb34a307fbc3671b46340"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infuraEthereum/latest/actions/get-transaction-receipt?${params}`, {
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
| `params[0]` | string | yes | The transaction hash to inspect. Example: `0x714d09606652a43a4f47cf7f59b88659bdf54a4fa7eeb34a307fbc3671b46340`. |

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
| `blockHash` | string | The block hash containing the transaction. |
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

Through the native Infura Ethereum API, this operation is `POST /v3/:apiKey` (base URL `https://mainnet.infura.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction-receipt.md) for the provider-specific parameters and requirements.

