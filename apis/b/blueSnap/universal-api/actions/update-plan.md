# BlueSnap: Update Plan

Updates a plan in BlueSnap.

```
PUT https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/update-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlueSnap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/update-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "planId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/update-plan', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "planId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `planId` | string | yes | Billing plan ID. |
| `status` | string | no | Plan status for updates (ACTIVE or INACTIVE). |

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

Through the native BlueSnap API, this operation is `PUT /recurring/plans/:planId` (base URL `https://sandbox.bluesnap.com/services/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-plan.md) for the provider-specific parameters and requirements.

