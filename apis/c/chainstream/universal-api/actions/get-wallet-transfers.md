# Chainstream: Get Wallet Transfers

Retrieves wallet transfers from Chainstream.

```
GET https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-wallet-transfers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chainstream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-wallet-transfers?connectionId=$CONNECTION_ID&chain=string&walletAddress=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chain": "string",
  "walletAddress": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-wallet-transfers?${params}`, {
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
| `chain` | string | yes | A chain name listed in supported networks. |
| `walletAddress` | string | yes | An address of a wallet. |
| `limit` | number | no | Number of results per page. Default: `20`. |
| `direction` | string | no | Pagination direction (next or prev). Default: `next`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cursor` | string | no | Pagination cursor. |
| `tokenAddress` | string | no | An address of a token. |
| `fromTimestamp` | number | no | Filter transfers after this timestamp (Unix epoch seconds). |
| `toTimestamp` | number | no | Filter transfers before this timestamp (Unix epoch seconds). |
| `minTokenAmount` | string | no | Minimum token amount filter (inclusive). |
| `maxTokenAmount` | string | no | Maximum token amount filter (inclusive). |
| `minTokenAmountInUsd` | string | no | Minimum token amount in USD filter (inclusive). |
| `maxTokenAmountInUsd` | string | no | Maximum token amount in USD filter (inclusive). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "amount": "string",
          "amountInUsd": "string",
          "blockTimestamp": 1,
          "fromAddress": "string",
          "id": "string",
          "toAddress": "string",
          "tokenAddress": "string",
          "transactionSignature": "string",
          "transferType": "string"
        }
      ],
      "endCursor": "string",
      "hasNext": true,
      "hasPrev": true,
      "startCursor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].amount` | string |  |
| `data[].amountInUsd` | string |  |
| `data[].blockTimestamp` | number |  |
| `data[].fromAddress` | string |  |
| `data[].id` | string |  |
| `data[].toAddress` | string |  |
| `data[].tokenAddress` | string |  |
| `data[].transactionSignature` | string |  |
| `data[].transferType` | string |  |
| `endCursor` | string |  |
| `hasNext` | boolean |  |
| `hasPrev` | boolean |  |
| `startCursor` | string |  |

## Native endpoint

Through the native Chainstream API, this operation is `GET /v2/wallet/:chain/:walletAddress/transfers` (base URL `https://api.chainstream.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-wallet-transfers.md) for the provider-specific parameters and requirements.

