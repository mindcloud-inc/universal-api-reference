# 1Shot: Get Wallet

Retrieves wallet details from 1Shot API.

```
GET https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/get-wallet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1Shot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/get-wallet?connectionId=$CONNECTION_ID&walletId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "walletId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/get-wallet?${params}`, {
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
| `walletId` | string | yes | The internal UUID of the wallet. |
| `includeBalances` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountAddress": "string",
      "accountBalanceDetails": {
        "accountAddress": "string",
        "balance": "string",
        "chainId": 1,
        "decimals": 1,
        "ticker": "string",
        "tokenAddress": "string",
        "type": 1
      },
      "businessId": "string",
      "chainId": 1,
      "created": 1,
      "description": "string",
      "erc7702ContractAddress": "string",
      "id": "string",
      "isAdmin": true,
      "lowBalanceThreshold": "string",
      "name": "Ava Chen",
      "permit2AuthorizedContractAddresses": [
        "string"
      ],
      "updated": 1,
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountAddress` | string |  |
| `accountBalanceDetails.accountAddress` | string |  |
| `accountBalanceDetails.balance` | string |  |
| `accountBalanceDetails.chainId` | number |  |
| `accountBalanceDetails.decimals` | number |  |
| `accountBalanceDetails.ticker` | string |  |
| `accountBalanceDetails.tokenAddress` | string |  |
| `accountBalanceDetails.type` | number |  |
| `businessId` | string |  |
| `chainId` | number |  |
| `created` | number |  |
| `description` | string |  |
| `erc7702ContractAddress` | string |  |
| `id` | string |  |
| `isAdmin` | boolean |  |
| `lowBalanceThreshold` | string |  |
| `name` | string |  |
| `permit2AuthorizedContractAddresses[]` | string |  |
| `updated` | number |  |
| `userId` | string |  |

## Native endpoint

Through the native 1Shot API, this operation is `GET /wallets/:walletId` (base URL `https://api.1shotapi.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-wallet.md) for the provider-specific parameters and requirements.

