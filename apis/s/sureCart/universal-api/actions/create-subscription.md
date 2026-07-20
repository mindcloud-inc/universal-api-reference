# SureCart: Create Subscription



```
POST https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/create-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureCart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/create-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscription.customer": "8fd47739-8749-4636-85b4-65ead1a58ee5",
  "subscription.price": "41fae5ec-1777-4142-a13b-c5adfea5cabc"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/create-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscription.customer": "8fd47739-8749-4636-85b4-65ead1a58ee5",
    "subscription.price": "41fae5ec-1777-4142-a13b-c5adfea5cabc"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscription.customer` | string | yes | The customer ID to subscribe. Example: `8fd47739-8749-4636-85b4-65ead1a58ee5`. |
| `subscription.price` | string | yes | The recurring price ID for the subscription. Example: `41fae5ec-1777-4142-a13b-c5adfea5cabc`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscription.paymentMethod` | string | no | Optional payment method ID for paid subscriptions. Example: `f137eb11-ee2b-4cc3-84e5-46ce1ae486df`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cancelAtPeriodEnd": true,
      "createdAt": 1,
      "currency": "string",
      "currentCancellationAct": "string",
      "currentPeriod": "string",
      "currentPeriodEndAt": 1,
      "currentPeriodStartAt": 1,
      "customer": "string",
      "endBehavior": "string",
      "id": "string",
      "liveMode": true,
      "manualPayment": true,
      "metadata": {},
      "object": "string",
      "pendingUpdate": {},
      "portalUrl": "https://example.com",
      "price": "string",
      "purchase": "string",
      "quantity": 1,
      "status": "string",
      "subtotalAmount": 1,
      "taxEnabled": true,
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cancelAtPeriodEnd` | boolean |  |
| `createdAt` | number |  |
| `currency` | string |  |
| `currentCancellationAct` | string |  |
| `currentPeriod` | string |  |
| `currentPeriodEndAt` | number |  |
| `currentPeriodStartAt` | number |  |
| `customer` | string |  |
| `endBehavior` | string |  |
| `id` | string |  |
| `liveMode` | boolean |  |
| `manualPayment` | boolean |  |
| `metadata` | object |  |
| `object` | string |  |
| `pendingUpdate` | object |  |
| `portalUrl` | string |  |
| `price` | string |  |
| `purchase` | string |  |
| `quantity` | number |  |
| `status` | string |  |
| `subtotalAmount` | number |  |
| `taxEnabled` | boolean |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native SureCart API, this operation is `POST v1/subscriptions` (base URL `https://api.surecart.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subscription.md) for the provider-specific parameters and requirements.

