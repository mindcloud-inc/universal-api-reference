# Quantum Digital: Create Payment Method



```
POST https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/create-payment-method
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quantum Digital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/create-payment-method" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "billingAddress1": "string",
  "billingCity": "string",
  "billingCountry": "Canada",
  "billingPostalCode": "string",
  "billingStateProvince": "string",
  "creditCardNumber": "string",
  "creditCardType": "American Express",
  "expMonth": "string",
  "expYear": "string",
  "nameOnCard": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/create-payment-method', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "billingAddress1": "string",
    "billingCity": "string",
    "billingCountry": "Canada",
    "billingPostalCode": "string",
    "billingStateProvince": "string",
    "creditCardNumber": "string",
    "creditCardType": "American Express",
    "expMonth": "string",
    "expYear": "string",
    "nameOnCard": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `billingAddress1` | string | yes |  |
| `billingAddress2` | string | no |  |
| `billingCity` | string | yes |  |
| `billingCountry` | list | yes | One of: `Canada`, `United States`. |
| `billingPostalCode` | string | yes |  |
| `billingStateProvince` | string | yes |  |
| `creditCardNumber` | string | yes |  |
| `creditCardType` | list | yes | One of: `American Express`, `Discover`, `Mastercard`, `Visa`. |
| `expMonth` | string | yes |  |
| `expYear` | string | yes |  |
| `nameOnCard` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the payment method was created successfully. |

## Native endpoint

Through the native Quantum Digital API, this operation is `POST /devplatform/billing/:dashboardAccountId/paymentmethods` (base URL `https://api.quantumdigital.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment-method.md) for the provider-specific parameters and requirements.

