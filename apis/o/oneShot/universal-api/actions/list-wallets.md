# 1Shot: List Wallets

Retrieves wallet records from 1Shot API.

```
GET https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/list-wallets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1Shot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/list-wallets?connectionId=$CONNECTION_ID&businessId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "businessId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/list-wallets?${params}`, {
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
| `businessId` | string | yes | The internal UUID of the business. |
| `chainId` | number | no |  |
| `name` | string | no |  |

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

Through the native 1Shot API, this operation is `GET /business/:businessId/wallets` (base URL `https://api.1shotapi.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-wallets.md) for the provider-specific parameters and requirements.

