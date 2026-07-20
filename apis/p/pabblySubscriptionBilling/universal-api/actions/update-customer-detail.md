# Pabbly Subscription Billing: Update Customer Detail



```
PUT https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/update-customer-detail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/update-customer-detail" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/update-customer-detail', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `billingAddress` | string | no | Update the billing address of the customer. |
| `companyName` | string | no | Update the Customer's company name. |
| `customerId` | string | no | Pabbly Customer ID. |
| `enableAffiliate` | string | no | Value will be yes/no |
| `enablePortal` | string | no | Value will be yes/no |
| `firstName` | string | no | Update the First Name of your customer. |
| `lastName` | string | no | Update the Last Name of your customer. |
| `phone` | string | no | Update the Customer's phone number. |
| `shippingAddress` | string | no | Update the shipping address of the customer. |
| `website` | string | no | Update the Customer's website name. |

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
        "stateCode": "string",
        "street1": "string",
        "street2": "string",
        "zipCode": "string"
      },
      "companyName": "Ava Chen",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "emailId": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "isAffiliate": true,
      "lastName": "Chen",
      "phone": "string",
      "portalStatus": true,
      "shippingAddress": {
        "attention": "string",
        "city": "string",
        "country": "string",
        "state": "string",
        "stateCode": "string",
        "street1": "string",
        "street2": "string",
        "zipCode": "string"
      },
      "updatedAt": "2026-05-07T12:00:00.000Z"
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
| `billingAddress.stateCode` | string |  |
| `billingAddress.street1` | string |  |
| `billingAddress.street2` | string |  |
| `billingAddress.zipCode` | string |  |
| `companyName` | string |  |
| `createdAt` | date |  |
| `emailId` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `isAffiliate` | boolean |  |
| `lastName` | string |  |
| `phone` | string |  |
| `portalStatus` | boolean |  |
| `shippingAddress.attention` | string |  |
| `shippingAddress.city` | string |  |
| `shippingAddress.country` | string |  |
| `shippingAddress.state` | string |  |
| `shippingAddress.stateCode` | string |  |
| `shippingAddress.street1` | string |  |
| `shippingAddress.street2` | string |  |
| `shippingAddress.zipCode` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `PUT /v1/customer/:customerId` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer-detail.md) for the provider-specific parameters and requirements.

