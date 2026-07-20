# Pabbly Subscription Billing: Create Customer With Subscription



```
POST https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/create-customer-with-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/create-customer-with-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/create-customer-with-subscription', {
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
| `addons` | string | no | Addons. |
| `cardNumber` | string | no | Pabbly Card Number. |
| `city` | string | no | Pabbly City. |
| `country` | string | no | Pabbly Country. |
| `couponCode` | string | no | Pabbly Coupon Code. |
| `cvv` | string | no | Pabbly CVV. |
| `email` | string | no | Pabbly Email. |
| `firstName` | string | no | Pabbly First Name. |
| `gatewayId` | string | no | Unique Id of the payment gateway from which the payment is processed. |
| `gatewayType` | string | no | One of paypal, stripe, test, custom, connect, offline, or free. |
| `isAffiliate` | string | no | To create this customer as a Affiliate, it can be boolean value true or false. |
| `lastName` | string | no | Pabbly Last Name. |
| `month` | string | no | Pabbly Month. |
| `planAmount` | string | no | Enter only the plan amount without adding the currency symbol. |
| `planId` | string | no | Unique Id of the plan which you will assign to this customer. |
| `quantity` | string | no | Quantity of the plan. |
| `redirectTo` | string | no | The customer will be redirected to this link after successful payment. |
| `state` | string | no | Pabbly State. |
| `street` | string | no | Pabbly Street. |
| `taxId` | string | no | Tax ID recorded for a customer. |
| `year` | string | no | Pabbly Year. |
| `zipCode` | string | no | Pabbly Zip Code. |

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
        "isAffiliate": true,
        "referralId": "string",
        "shippingAddress": {
          "city": "string",
          "country": "string",
          "state": "string",
          "stateCode": "string",
          "street1": "string",
          "zipCode": "string"
        }
      },
      "user": {
        "addressLine1": "string",
        "addressLine2": "string",
        "city": "string",
        "country": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "currency": "string",
        "currencySymbol": "string",
        "dateFormat": "2026-05-07T12:00:00.000Z",
        "email": "ava@example.com",
        "facebookUrl": "https://example.com",
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "mobile": "string",
        "phone": "string",
        "state": "string",
        "timeZone": "string",
        "twitterUrl": "https://example.com",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "verified": "string",
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
| `customer.billingAddress.city` | string |  |
| `customer.billingAddress.country` | string |  |
| `customer.billingAddress.state` | string |  |
| `customer.billingAddress.stateCode` | string |  |
| `customer.billingAddress.street1` | string |  |
| `customer.billingAddress.zipCode` | string |  |
| `customer.isAffiliate` | boolean |  |
| `customer.referralId` | string |  |
| `customer.shippingAddress.city` | string |  |
| `customer.shippingAddress.country` | string |  |
| `customer.shippingAddress.state` | string |  |
| `customer.shippingAddress.stateCode` | string |  |
| `customer.shippingAddress.street1` | string |  |
| `customer.shippingAddress.zipCode` | string |  |
| `user.addressLine1` | string |  |
| `user.addressLine2` | string |  |
| `user.city` | string |  |
| `user.country` | string |  |
| `user.createdAt` | date |  |
| `user.currency` | string |  |
| `user.currencySymbol` | string |  |
| `user.dateFormat` | date |  |
| `user.email` | string |  |
| `user.facebookUrl` | string |  |
| `user.firstName` | string |  |
| `user.id` | string |  |
| `user.lastName` | string |  |
| `user.mobile` | string |  |
| `user.phone` | string |  |
| `user.state` | string |  |
| `user.timeZone` | string |  |
| `user.twitterUrl` | string |  |
| `user.updatedAt` | date |  |
| `user.verified` | string |  |
| `user.zipCode` | string |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `POST /v1/subscription` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer-with-subscription.md) for the provider-specific parameters and requirements.

