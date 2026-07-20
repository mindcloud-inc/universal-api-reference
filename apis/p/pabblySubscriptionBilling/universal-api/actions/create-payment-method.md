# Pabbly Subscription Billing: Create Payment Method



```
POST https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/create-payment-method
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/create-payment-method" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/create-payment-method', {
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
| `cardNumber` | string | no |  |
| `city` | string | no |  |
| `country` | string | no |  |
| `customerId` | string | no |  |
| `cvv` | string | no |  |
| `email` | string | no |  |
| `firstName` | string | no |  |
| `gatewayType` | string | no |  |
| `lastName` | string | no |  |
| `month` | string | no |  |
| `state` | string | no |  |
| `street` | string | no |  |
| `year` | string | no |  |
| `zipCode` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "gateway": {
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gateway.id` | string |  |
| `gateway.name` | string |  |
| `gateway.type` | string |  |
| `id` | string |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `POST /v1/paymentmethod/:customerId` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment-method.md) for the provider-specific parameters and requirements.

