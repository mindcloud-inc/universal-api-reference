# Copperx: Get Payment Setting

Retrieves organization payment settings from Copperx.

```
GET https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-payment-setting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Copperx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-payment-setting?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-payment-setting?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "allowedChains": [
        {}
      ],
      "allowedCurrencies": [
        "string"
      ],
      "allowSplitPayments": true,
      "allowSwap": true,
      "applyFee": true,
      "applyGasFee": true,
      "applyWalletScreening": true,
      "createdAt": "string",
      "feePercentage": 1,
      "id": "string",
      "paymentMethodTypes": [
        "string"
      ],
      "preferredChainId": 1,
      "preferredCurrency": "string",
      "slippagePercentage": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowedChains` | array<object> |  |
| `allowedCurrencies` | array<string> |  |
| `allowSplitPayments` | boolean |  |
| `allowSwap` | boolean |  |
| `applyFee` | boolean |  |
| `applyGasFee` | boolean |  |
| `applyWalletScreening` | boolean |  |
| `createdAt` | string |  |
| `feePercentage` | number |  |
| `id` | string |  |
| `paymentMethodTypes` | array<string> |  |
| `preferredChainId` | number |  |
| `preferredCurrency` | string |  |
| `slippagePercentage` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Copperx API, this operation is `GET /organization/payment-setting` (base URL `https://api.copperx.dev/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payment-setting.md) for the provider-specific parameters and requirements.

