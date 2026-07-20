# Pabbly Subscription Billing: Create Customer



```
POST https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/create-customer', {
  method: 'POST',
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `billingAddress` | string | no | Pabbly Billing Address. |
| `companyName` | string | no | Pabbly Company Name. |
| `emailId` | string | no | Email address of your customer. |
| `firstName` | string | no | First Name of your customer |
| `isAffiliate` | string | no | To create this customer as a Affiliate, It can be boolean value true or false |
| `lastName` | string | no | Last Name of your customer. |
| `phone` | string | no | Pabbly Phone. |
| `shippingAddress` | string | no | Pabbly Shipping Address. |
| `website` | string | no | Pabbly Website. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingAddress": {
        "attention": "string",
        "city": "string",
        "country": "string",
        "state": "string",
        "street1": "string",
        "street2": "string",
        "zipCode": "string"
      },
      "companyName": "Ava Chen",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "emailId": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "phone": "string",
      "shippingAddress": {
        "attention": "string",
        "city": "string",
        "country": "string",
        "state": "string",
        "street1": "string",
        "street2": "string",
        "zipCode": "string"
      },
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingAddress.attention` | string |  |
| `billingAddress.city` | string |  |
| `billingAddress.country` | string |  |
| `billingAddress.state` | string |  |
| `billingAddress.street1` | string |  |
| `billingAddress.street2` | string |  |
| `billingAddress.zipCode` | string |  |
| `companyName` | string |  |
| `createdAt` | date |  |
| `emailId` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `phone` | string |  |
| `shippingAddress.attention` | string |  |
| `shippingAddress.city` | string |  |
| `shippingAddress.country` | string |  |
| `shippingAddress.state` | string |  |
| `shippingAddress.street1` | string |  |
| `shippingAddress.street2` | string |  |
| `shippingAddress.zipCode` | string |  |
| `updatedAt` | date |  |
| `website` | string |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `POST /v1/customer` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

