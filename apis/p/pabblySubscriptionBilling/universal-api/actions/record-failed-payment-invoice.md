# Pabbly Subscription Billing: Record Failed Payment Invoice



```
PUT https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/record-failed-payment-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/record-failed-payment-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/record-failed-payment-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "customer": {
        "billingAddress": {
          "city": "string",
          "country": "string",
          "state": "string",
          "stateCode": "string",
          "street1": "string",
          "zipCode": "string"
        },
        "companyName": "Ava Chen",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "emailId": "ava@example.com",
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "phone": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "website": "string"
      },
      "product": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "id": "string",
        "productName": "Ava Chen",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customer.billingAddress.city` | string |  |
| `customer.billingAddress.country` | string |  |
| `customer.billingAddress.state` | string |  |
| `customer.billingAddress.stateCode` | string |  |
| `customer.billingAddress.street1` | string |  |
| `customer.billingAddress.zipCode` | string |  |
| `customer.companyName` | string |  |
| `customer.createdAt` | date |  |
| `customer.emailId` | string |  |
| `customer.firstName` | string |  |
| `customer.id` | string |  |
| `customer.lastName` | string |  |
| `customer.phone` | string |  |
| `customer.updatedAt` | date |  |
| `customer.website` | string |  |
| `product.createdAt` | date |  |
| `product.description` | string |  |
| `product.id` | string |  |
| `product.productName` | string |  |
| `product.updatedAt` | date |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `POST /v1/invoice/failedpayment/:invoiceId` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/record-failed-payment-invoice.md) for the provider-specific parameters and requirements.

