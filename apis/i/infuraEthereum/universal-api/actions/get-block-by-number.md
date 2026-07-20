# Infura Ethereum: Get Block By Number

Retrieves a block from Infura Ethereum by number.

```
GET https://connect.mindcloud.co/v1/universal/infuraEthereum/latest/actions/get-block-by-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infura Ethereum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infuraEthereum/latest/actions/get-block-by-number?connectionId=$CONNECTION_ID&params%5B0%5D=0x17d6510&params%5B1%5D=false" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "params[0]": "0x17d6510",
  "params[1]": "false"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infuraEthereum/latest/actions/get-block-by-number?${params}`, {
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
| `params[0]` | string | yes | The block number or canonical tag to retrieve. Example: `0x17d6510`. |
| `params[1]` | boolean | yes | Whether to expand transactions to full objects instead of transaction hashes. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseFeePerGas": "string",
      "gasLimit": "string",
      "gasUsed": "string",
      "hash": "string",
      "miner": "string",
      "number": "string",
      "parentHash": "string",
      "size": "string",
      "timestamp": "string",
      "transactions": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseFeePerGas` | string | The base fee per gas for the block as a hex quantity. |
| `gasLimit` | string | The block gas limit as a hex quantity. |
| `gasUsed` | string | The gas used in the block as a hex quantity. |
| `hash` | string | The block hash. |
| `miner` | string | The block beneficiary address. |
| `number` | string | The block number as a hex quantity. |
| `parentHash` | string | The parent block hash. |
| `size` | string | The block size as a hex quantity. |
| `timestamp` | string | The block timestamp as a hex quantity. |
| `transactions` | array<string> | The transaction hashes included in the block. |

## Native endpoint

Through the native Infura Ethereum API, this operation is `POST /v3/:apiKey` (base URL `https://mainnet.infura.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-block-by-number.md) for the provider-specific parameters and requirements.

