# BigCommerce (B2B): Get Company Payment Methods



```
PUT https://connect.mindcloud.co/v1/universal/bigCommerceB2B/latest/actions/get-company-payment-methods
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigCommerce (B2B) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bigCommerceB2B/latest/actions/get-company-payment-methods" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bigCommerceB2B/latest/actions/get-company-payment-methods', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "availableCredit": {},
        "creditCurrency": "string",
        "creditEnabled": true,
        "creditHold": true,
        "limitPurchases": true
      },
      "meta": {
        "message": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data.availableCredit` | object |  |
| `data.creditCurrency` | string |  |
| `data.creditEnabled` | boolean |  |
| `data.creditHold` | boolean |  |
| `data.limitPurchases` | boolean |  |
| `meta.message` | string |  |

## Native endpoint

Through the native BigCommerce (B2B) API, this operation is `GET companies/:companyId/payments` (base URL `https://api-b2b.bigcommerce.com/api/v3/io/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-payment-methods.md) for the provider-specific parameters and requirements.

