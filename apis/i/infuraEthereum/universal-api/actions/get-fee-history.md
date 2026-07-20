# Infura Ethereum: Get Fee History

Retrieves fee history from Infura Ethereum.

```
GET https://connect.mindcloud.co/v1/universal/infuraEthereum/latest/actions/get-fee-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infura Ethereum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infuraEthereum/latest/actions/get-fee-history?connectionId=$CONNECTION_ID&params%5B0%5D=0x4&params%5B1%5D=latest" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "params[0]": "0x4",
  "params[1]": "latest"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infuraEthereum/latest/actions/get-fee-history?${params}`, {
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
| `params[0]` | string | yes | How many recent blocks to include, as a hex quantity. Example: `0x4`. |
| `params[1]` | string | yes | The newest block to anchor the history window, such as latest or a hex block number. Example: `latest`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseFeePerBlobGas": [
        "string"
      ],
      "baseFeePerGas": [
        "string"
      ],
      "blobGasUsedRatio": [
        1
      ],
      "gasUsedRatio": [
        1
      ],
      "oldestBlock": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseFeePerBlobGas` | array<string> | Blob base fee for each returned block, plus the next block blob base fee when available. |
| `baseFeePerGas` | array<string> | Base fee per gas for each returned block, plus the next block base fee. |
| `blobGasUsedRatio` | array<number> | Blob gas used ratio for each returned block when available. |
| `gasUsedRatio` | array<number> | Gas used ratio for each returned block. |
| `oldestBlock` | string | The oldest block in the requested fee history window as a hex quantity. |

## Native endpoint

Through the native Infura Ethereum API, this operation is `POST /v3/:apiKey` (base URL `https://mainnet.infura.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-fee-history.md) for the provider-specific parameters and requirements.

