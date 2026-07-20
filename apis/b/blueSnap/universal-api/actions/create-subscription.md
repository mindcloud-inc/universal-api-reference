# BlueSnap: Create Subscription

Creates a subscription in BlueSnap.

```
POST https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/create-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlueSnap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/create-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "planId": "string",
  "vaultedShopperId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/create-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "planId": "string",
    "vaultedShopperId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `planId` | string | yes | Billing plan ID for the subscription. |
| `vaultedShopperId` | string | yes | Vaulted shopper ID to attach to the subscription. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "charge": {
        "chargeId": 1,
        "transactionId": "string"
      },
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
| `charge.chargeId` | number | Initial charge ID. |
| `charge.transactionId` | string | Initial charge transaction ID. |
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

Through the native BlueSnap API, this operation is `POST /recurring/subscriptions` (base URL `https://sandbox.bluesnap.com/services/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subscription.md) for the provider-specific parameters and requirements.

