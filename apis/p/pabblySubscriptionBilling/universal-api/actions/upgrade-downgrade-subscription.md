# Pabbly Subscription Billing: Upgrade Downgrade Subscription



```
PUT https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/upgrade-downgrade-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/upgrade-downgrade-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/upgrade-downgrade-subscription', {
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
| `activatedAtVal` | string | no |  |
| `addons` | string | no |  |
| `cardId` | string | no |  |
| `couponCode` | string | no |  |
| `customerId` | string | no |  |
| `paymentMode` | string | no |  |
| `paymentTerm` | string | no |  |
| `planId` | string | no |  |
| `price` | string | no |  |
| `quantity` | string | no |  |
| `setupFee` | string | no |  |
| `subscriptionId` | string | no |  |
| `updateReason` | string | no |  |

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
        "createdAt": "2026-05-07T12:00:00.000Z",
        "credit": "string",
        "emailId": "ava@example.com",
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "updatedAt": "2026-05-07T12:00:00.000Z"
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
        "ipAddress": "string",
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
| `customer.createdAt` | date |  |
| `customer.credit` | string |  |
| `customer.emailId` | string |  |
| `customer.firstName` | string |  |
| `customer.id` | string |  |
| `customer.lastName` | string |  |
| `customer.updatedAt` | date |  |
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
| `user.ipAddress` | string |  |
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

Through the native Pabbly Subscription Billing API, this operation is `PUT /v1/subscription/:subscriptionId/upgrade-downgrade` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upgrade-downgrade-subscription.md) for the provider-specific parameters and requirements.

