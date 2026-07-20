# PayWhirl: Create Plan

Creates a new subscription plan in PayWhirl.

```
POST https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/create-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayWhirl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/create-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/create-plan', {
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
      "active": 1,
      "billingAmount": 1,
      "billingFrequency": "string",
      "billingInterval": 1,
      "createdAt": "string",
      "currency": "string",
      "deletedAt": "string",
      "description": "string",
      "enabled": 1,
      "id": 1,
      "image": "string",
      "installments": 1,
      "metadata": "string",
      "name": "Ava Chen",
      "requireTax": 1,
      "setupFee": 1,
      "setupFeeType": "string",
      "sku": "string",
      "trialDays": 1,
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
| `active` | number |  |
| `billingAmount` | number |  |
| `billingFrequency` | string |  |
| `billingInterval` | number |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `deletedAt` | string |  |
| `description` | string |  |
| `enabled` | number |  |
| `id` | number |  |
| `image` | string |  |
| `installments` | number |  |
| `metadata` | string |  |
| `name` | string |  |
| `requireTax` | number |  |
| `setupFee` | number |  |
| `setupFeeType` | string |  |
| `sku` | string |  |
| `trialDays` | number |  |
| `updatedAt` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native PayWhirl API, this operation is `POST /create/plan` (base URL `https://api.paywhirl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-plan.md) for the provider-specific parameters and requirements.

