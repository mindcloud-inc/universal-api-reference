# Quantum Digital: List Payment Methods



```
GET https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/list-payment-methods
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quantum Digital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/list-payment-methods?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/list-payment-methods?${params}`, {
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
      "creditCardType": "string",
      "expMonth": "string",
      "expYear": "string",
      "maskedCreditCardNumber": "string",
      "nameOnCard": "Ava Chen",
      "paymentMethodStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditCardType` | string | Card brand code. |
| `expMonth` | string | Expiration month. |
| `expYear` | string | Expiration year. |
| `maskedCreditCardNumber` | string | Masked credit card number. |
| `nameOnCard` | string | Name displayed on the payment method. |
| `paymentMethodStatus` | string | Current status for the payment method. |

## Native endpoint

Through the native Quantum Digital API, this operation is `GET /devplatform/billing/:dashboardAccountId/paymentmethods` (base URL `https://api.quantumdigital.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payment-methods.md) for the provider-specific parameters and requirements.

