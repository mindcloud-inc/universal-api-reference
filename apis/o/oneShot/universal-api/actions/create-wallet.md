# 1Shot: Create Wallet

Creates a new wallet in 1Shot API.

```
POST https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/create-wallet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1Shot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/create-wallet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "businessId": "string",
  "chainId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/create-wallet', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "businessId": "string",
    "chainId": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `businessId` | string | yes |  |
| `chainId` | number | yes |  |
| `name` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountAddress": "string",
      "accountBalanceDetails": {},
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
| `accountBalanceDetails` | object |  |
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

Through the native 1Shot API, this operation is `POST /business/:businessId/wallets` (base URL `https://api.1shotapi.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-wallet.md) for the provider-specific parameters and requirements.

