# Pabbly Subscription Billing: Record Payment Invoice



```
PUT https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/record-payment-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/record-payment-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/record-payment-invoice', {
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
      "user": {
        "addressLine1": "string",
        "addressLine2": "string",
        "city": "string",
        "country": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "currency": "string",
        "email": "ava@example.com",
        "facebookUrl": "https://example.com",
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "lockoutCount": 1,
        "mobile": "string",
        "parent": "string",
        "phone": "string",
        "process": "string",
        "state": "string",
        "status": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "zipCode": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `user.addressLine1` | string |  |
| `user.addressLine2` | string |  |
| `user.city` | string |  |
| `user.country` | string |  |
| `user.createdAt` | date |  |
| `user.currency` | string |  |
| `user.email` | string |  |
| `user.facebookUrl` | string |  |
| `user.firstName` | string |  |
| `user.id` | string |  |
| `user.lastName` | string |  |
| `user.lockoutCount` | number |  |
| `user.mobile` | string |  |
| `user.parent` | string |  |
| `user.phone` | string |  |
| `user.process` | string |  |
| `user.state` | string |  |
| `user.status` | string |  |
| `user.updatedAt` | date |  |
| `user.zipCode` | string |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `POST /v1/invoice/recordpayment/:invoiceId` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/record-payment-invoice.md) for the provider-specific parameters and requirements.

