# SureCart: Create Price



```
POST https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/create-price
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureCart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/create-price" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "price.product_id": "2fed6132-36c1-4761-b3a2-e30af3c4b0dd",
  "price.amount": "2900",
  "price.currency": "usd"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/create-price', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "price.product_id": "2fed6132-36c1-4761-b3a2-e30af3c4b0dd",
    "price.amount": "2900",
    "price.currency": "usd"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `price.product_id` | string | yes | The product ID this price belongs to. Example: `2fed6132-36c1-4761-b3a2-e30af3c4b0dd`. |
| `price.amount` | number | yes | The amount in cents to charge for this price. Example: `2900`. |
| `price.currency` | string | yes | Three-letter ISO currency code in lowercase. Example: `usd`. |
| `price.name` | string | no | The display name for this price. Example: `Standard Price`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adHoc": true,
      "adHocMaxAmount": 1,
      "adHocMinAmount": 1,
      "amount": 1,
      "archived": true,
      "createdAt": 1,
      "currency": "string",
      "currentVersion": true,
      "fullAmount": 1,
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "portalSubscriptionUpdateEnabled": true,
      "position": 1,
      "product": "string",
      "recurringEndBehavior": "string",
      "recurringInterval": "string",
      "recurringIntervalCount": 1,
      "recurringPeriodCount": 1,
      "renewalPrice": "string",
      "restartSubscriptionOnCompleted": true,
      "revokeAfterDays": 1,
      "revokePurchasesOnCompleted": true,
      "scratchAmount": 1,
      "setupFeeAmount": 1,
      "setupFeeEnabled": true,
      "setupFeeName": "Ava Chen",
      "setupFeeTrialEnabled": true,
      "trialDurationDays": 1,
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adHoc` | boolean |  |
| `adHocMaxAmount` | number |  |
| `adHocMinAmount` | number |  |
| `amount` | number |  |
| `archived` | boolean |  |
| `createdAt` | number |  |
| `currency` | string |  |
| `currentVersion` | boolean |  |
| `fullAmount` | number |  |
| `id` | string |  |
| `name` | string |  |
| `object` | string |  |
| `portalSubscriptionUpdateEnabled` | boolean |  |
| `position` | number |  |
| `product` | string |  |
| `recurringEndBehavior` | string |  |
| `recurringInterval` | string |  |
| `recurringIntervalCount` | number |  |
| `recurringPeriodCount` | number |  |
| `renewalPrice` | string |  |
| `restartSubscriptionOnCompleted` | boolean |  |
| `revokeAfterDays` | number |  |
| `revokePurchasesOnCompleted` | boolean |  |
| `scratchAmount` | number |  |
| `setupFeeAmount` | number |  |
| `setupFeeEnabled` | boolean |  |
| `setupFeeName` | string |  |
| `setupFeeTrialEnabled` | boolean |  |
| `trialDurationDays` | number |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native SureCart API, this operation is `POST v1/prices` (base URL `https://api.surecart.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-price.md) for the provider-specific parameters and requirements.

