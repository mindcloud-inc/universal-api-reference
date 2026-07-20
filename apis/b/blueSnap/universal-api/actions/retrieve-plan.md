# BlueSnap: Retrieve Plan

Retrieves a plan from BlueSnap.

```
GET https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/retrieve-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlueSnap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/retrieve-plan?connectionId=$CONNECTION_ID&planId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "planId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/retrieve-plan?${params}`, {
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
| `planId` | string | yes | Billing plan ID. |

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

Through the native BlueSnap API, this operation is `GET /recurring/plans/:planId` (base URL `https://sandbox.bluesnap.com/services/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-plan.md) for the provider-specific parameters and requirements.

