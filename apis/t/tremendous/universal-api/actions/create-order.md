# Tremendous: Create Order

Creates a new order in Tremendous.

```
POST https://connect.mindcloud.co/v1/universal/tremendous/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tremendous `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tremendous/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "payment": {},
  "payment.funding_source_id": "string",
  "reward": {},
  "reward.delivery.method": "string",
  "reward.recipient.email": "ava@example.com",
  "reward.recipient.name": "Ava Chen",
  "reward.value.denomination": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tremendous/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "payment": {},
    "payment.funding_source_id": "string",
    "reward": {},
    "reward.delivery.method": "string",
    "reward.recipient.email": "ava@example.com",
    "reward.recipient.name": "Ava Chen",
    "reward.value.denomination": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `external_id` | string | no | Client-side idempotency key for the order |
| `payment` | object | yes | Payment object containing the funding source to charge |
| `payment.funding_source_id` | string | yes | Tremendous funding source ID used to pay for the order |
| `reward` | object | yes | Reward object describing value, recipient, and delivery |
| `reward.campaign_id` | string | no | Campaign ID that controls the reward products and presentation |
| `reward.delivery` | object | no | Reward delivery object |
| `reward.delivery.method` | string | yes | Delivery method for the reward |
| `reward.products[]` | array<string> | no | List of Tremendous product IDs available to the recipient |
| `reward.recipient` | object | no | Reward recipient object |
| `reward.recipient.email` | string | yes | Recipient email address |
| `reward.recipient.name` | string | yes | Recipient name |
| `reward.value` | object | no | Reward value object |
| `reward.value.currency_code` | string | no | ISO currency code for the reward value |
| `reward.value.denomination` | number | yes | Monetary amount of the reward |

## Response

```json
{
  "success": true,
  "data": [
    {
      "order": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `order` | object |  |

## Native endpoint

Through the native Tremendous API, this operation is `POST /orders` (base URL `https://testflight.tremendous.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

