# Infura Ethereum: Get Logs

Retrieves logs from Infura Ethereum.

```
GET https://connect.mindcloud.co/v1/universal/infuraEthereum/latest/actions/get-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infura Ethereum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infuraEthereum/latest/actions/get-logs?connectionId=$CONNECTION_ID&params%5B0%5D%5Baddress%5D=0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2&params%5B0%5D%5BfromBlock%5D=0x17d6506&params%5B0%5D%5BtoBlock%5D=0x17d6510" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "params[0][address]": "0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2",
  "params[0][fromBlock]": "0x17d6506",
  "params[0][toBlock]": "0x17d6510"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infuraEthereum/latest/actions/get-logs?${params}`, {
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
| `params[0][address]` | string | yes | Filter logs to one contract address. Example: `0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2`. |
| `params[0][fromBlock]` | string | yes | The starting block number or tag for the log search. Example: `0x17d6506`. |
| `params[0][toBlock]` | string | yes | The ending block number or tag for the log search. Example: `0x17d6510`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "blockHash": "string",
      "blockNumber": "string",
      "data": "string",
      "logIndex": "string",
      "removed": true,
      "topics": [
        "string"
      ],
      "transactionHash": "string",
      "transactionIndex": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | The contract address that emitted the log. |
| `blockHash` | string | The block hash containing the log. |
| `blockNumber` | string | The block number as a hex quantity. |
| `data` | string | The non-indexed event data as a hex string. |
| `logIndex` | string | The log index in the block as a hex quantity. |
| `removed` | boolean | Whether the log was removed due to a chain reorganization. |
| `topics` | array<string> | The indexed event topics. |
| `transactionHash` | string | The transaction hash containing the log. |
| `transactionIndex` | string | The transaction index in the block as a hex quantity. |

## Native endpoint

Through the native Infura Ethereum API, this operation is `POST /v3/:apiKey` (base URL `https://mainnet.infura.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-logs.md) for the provider-specific parameters and requirements.

