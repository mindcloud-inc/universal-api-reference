# Queue: Get Service Checkout

Retrieves a service checkout from Queue.

```
GET https://connect.mindcloud.co/v1/universal/queue/latest/actions/get-service-checkout
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Queue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/queue/latest/actions/get-service-checkout?connectionId=$CONNECTION_ID&serviceCheckoutId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "serviceCheckoutId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/queue/latest/actions/get-service-checkout?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `serviceCheckoutId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addonsPurchased": true,
      "archive": true,
      "cancelDate": "2026-05-07T12:00:00.000Z",
      "checkoutSessionId": "string",
      "completed": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "daysLeft": 1,
      "default": true,
      "disablePause": true,
      "id": "string",
      "monthsSinceCreation": 1,
      "paused": true,
      "pauseDate": "2026-05-07T12:00:00.000Z",
      "paypalSingleChargeData": {},
      "paypalSubscriptionData": {},
      "qty": 1,
      "retentionCouponUsed": true,
      "service": {},
      "servicePrice": {},
      "stripePaymentIntentId": "string",
      "stripeSubscriptionId": "string",
      "unsubscribedFeedback": "string",
      "unsubscribeReason": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addonsPurchased` | boolean |  |
| `archive` | boolean |  |
| `cancelDate` | date |  |
| `checkoutSessionId` | string |  |
| `completed` | boolean |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `daysLeft` | number |  |
| `default` | boolean |  |
| `disablePause` | boolean |  |
| `id` | string |  |
| `monthsSinceCreation` | number |  |
| `paused` | boolean |  |
| `pauseDate` | date |  |
| `paypalSingleChargeData` | object |  |
| `paypalSubscriptionData` | object |  |
| `qty` | number |  |
| `retentionCouponUsed` | boolean |  |
| `service` | object |  |
| `servicePrice` | object |  |
| `stripePaymentIntentId` | string |  |
| `stripeSubscriptionId` | string |  |
| `unsubscribedFeedback` | string |  |
| `unsubscribeReason` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Queue API, this operation is `GET service_checkouts/:service_checkout_id` (base URL `https://app.usequeue.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-service-checkout.md) for the provider-specific parameters and requirements.

