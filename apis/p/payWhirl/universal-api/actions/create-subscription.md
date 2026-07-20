# PayWhirl: Create Subscription

Creates a new subscription in PayWhirl.

```
POST https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/create-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayWhirl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/create-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/create-subscription', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "cancelAtPeriodEnd": 1,
      "createdAt": "string",
      "currentPeriodEnd": 1,
      "currentPeriodStart": 1,
      "customerId": 1,
      "deletedAt": "string",
      "id": 1,
      "installmentPlan": 1,
      "installmentsLeft": 1,
      "planId": 1,
      "quantity": 1,
      "trialEnd": 1,
      "trialStart": 1,
      "updatedAt": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cancelAtPeriodEnd` | number |  |
| `createdAt` | string |  |
| `currentPeriodEnd` | number |  |
| `currentPeriodStart` | number |  |
| `customerId` | number |  |
| `deletedAt` | string |  |
| `id` | number |  |
| `installmentPlan` | number |  |
| `installmentsLeft` | number |  |
| `planId` | number |  |
| `quantity` | number |  |
| `trialEnd` | number |  |
| `trialStart` | number |  |
| `updatedAt` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native PayWhirl API, this operation is `POST /subscribe/customer` (base URL `https://api.paywhirl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subscription.md) for the provider-specific parameters and requirements.

