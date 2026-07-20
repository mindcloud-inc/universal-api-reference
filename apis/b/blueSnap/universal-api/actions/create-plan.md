# BlueSnap: Create Plan

Creates a plan in BlueSnap.

```
POST https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/create-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlueSnap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/create-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "chargeFrequency": "MONTHLY",
  "currency": "USD",
  "recurringChargeAmount": "19.99"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/create-plan', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "chargeFrequency": "MONTHLY",
    "currency": "USD",
    "recurringChargeAmount": "19.99"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the billing plan. |
| `chargeFrequency` | string | yes | Charge frequency, e.g. MONTHLY. Default: `MONTHLY`. |
| `currency` | string | yes | Currency code (ISO 4217), e.g. USD. Default: `USD`. |
| `recurringChargeAmount` | string | yes | Recurring amount to charge. Default: `19.99`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chargeFrequency": "string",
      "currency": "string",
      "name": "Ava Chen",
      "planId": 1,
      "recurringChargeAmount": 1,
      "status": "string"
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
| `name` | string | Plan name. |
| `planId` | number | Plan ID. |
| `recurringChargeAmount` | number | Recurring charge amount. |
| `status` | string | Plan status. |

## Native endpoint

Through the native BlueSnap API, this operation is `POST /recurring/plans` (base URL `https://sandbox.bluesnap.com/services/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-plan.md) for the provider-specific parameters and requirements.

