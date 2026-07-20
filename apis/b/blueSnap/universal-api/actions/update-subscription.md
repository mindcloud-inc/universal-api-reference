# BlueSnap: Update Subscription

Updates a subscription in BlueSnap.

```
PUT https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/update-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlueSnap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/update-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriptionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/update-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriptionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscriptionId` | string | yes | Subscription ID. |
| `status` | string | no | Subscription status, e.g. ACTIVE or CANCELED. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chargeFrequency": "string",
      "currency": "string",
      "nextChargeDate": "string",
      "planId": 1,
      "quantity": 1,
      "recurringChargeAmount": 1,
      "status": "string",
      "subscriptionId": 1,
      "vaultedShopperId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chargeFrequency` | string | Charge frequency. |
| `currency` | string | Currency. |
| `nextChargeDate` | string | Next charge date. |
| `planId` | number | Plan ID. |
| `quantity` | number | Subscription quantity. |
| `recurringChargeAmount` | number | Recurring amount. |
| `status` | string | Subscription status. |
| `subscriptionId` | number | Subscription ID. |
| `vaultedShopperId` | number | Vaulted shopper ID. |

## Native endpoint

Through the native BlueSnap API, this operation is `PUT /recurring/subscriptions/:subscriptionId` (base URL `https://sandbox.bluesnap.com/services/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subscription.md) for the provider-specific parameters and requirements.

