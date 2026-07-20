# 1Shot: Get Chain Fees

Retrieves chain fee details from 1Shot API.

```
GET https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/get-chain-fees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1Shot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/get-chain-fees?connectionId=$CONNECTION_ID&chainId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chainId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/get-chain-fees?${params}`, {
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
| `chainId` | string | yes | The chain identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "effectiveGasPrice": "string",
      "gasPrice": "string",
      "history": {
        "blocks": [
          {
            "baseFeePerBlob": "string",
            "baseFeePerGas": "string",
            "blobGasUsedRatio": 1,
            "blockNumber": 1,
            "gasUsedRatio": 1,
            "reward100": "string",
            "reward20": "string",
            "reward50": "string"
          }
        ],
        "nextBaseFeePerGas": "string"
      },
      "maxFeePerGas": "string",
      "maxPriorityFeePerGas": "string",
      "nextBaseFeePerGas": "string",
      "pricingModel": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `effectiveGasPrice` | string |  |
| `gasPrice` | string |  |
| `history.blocks[].baseFeePerBlob` | string |  |
| `history.blocks[].baseFeePerGas` | string |  |
| `history.blocks[].blobGasUsedRatio` | number |  |
| `history.blocks[].blockNumber` | number |  |
| `history.blocks[].gasUsedRatio` | number |  |
| `history.blocks[].reward100` | string |  |
| `history.blocks[].reward20` | string |  |
| `history.blocks[].reward50` | string |  |
| `history.nextBaseFeePerGas` | string |  |
| `maxFeePerGas` | string |  |
| `maxPriorityFeePerGas` | string |  |
| `nextBaseFeePerGas` | string |  |
| `pricingModel` | string |  |

## Native endpoint

Through the native 1Shot API, this operation is `GET /chains/:chainId/fees` (base URL `https://api.1shotapi.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chain-fees.md) for the provider-specific parameters and requirements.

