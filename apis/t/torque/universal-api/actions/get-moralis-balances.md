# Torque: Get Moralis Balances



```
GET https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-moralis-balances
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Torque `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-moralis-balances?connectionId=$CONNECTION_ID&address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-moralis-balances?${params}`, {
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
| `address` | string | yes | Wallet address to query. |
| `chain` | string | no |  |
| `limit` | number | no | Maximum number of records to return. |
| `excludeSpam` | boolean | no |  |
| `excludeUnverifiedContracts` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": "string",
      "balanceFormatted": "string",
      "chainId": "string",
      "decimals": 1,
      "logoUri": "string",
      "name": "Ava Chen",
      "nativeToken": true,
      "portfolioPercentage": 1,
      "price": 1,
      "symbol": "string",
      "token": "string",
      "usdValue": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `balanceFormatted` | string |  |
| `chainId` | string |  |
| `decimals` | number |  |
| `logoUri` | string |  |
| `name` | string |  |
| `nativeToken` | boolean |  |
| `portfolioPercentage` | number |  |
| `price` | number |  |
| `symbol` | string |  |
| `token` | string |  |
| `usdValue` | number |  |

## Native endpoint

Through the native Torque API, this operation is `GET /moralis/balances` (base URL `https://app.torque.fi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-moralis-balances.md) for the provider-specific parameters and requirements.

