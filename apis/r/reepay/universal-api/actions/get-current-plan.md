# Reepay: Get Current Plan

Retrieves the current plan from Reepay.

```
GET https://connect.mindcloud.co/v1/universal/reepay/latest/actions/get-current-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reepay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reepay/latest/actions/get-current-plan?connectionId=$CONNECTION_ID&handle=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "handle": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reepay/latest/actions/get-current-plan?${params}`, {
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
| `handle` | string | yes | Plan handle from Reepay. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "amount_incl_vat": true,
      "created": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "deleted": "2026-05-07T12:00:00.000Z",
      "dunning_plan": "string",
      "effective_setup_fee_amount_incl_vat": true,
      "effective_setup_fee_vat": 1,
      "fixed_trial_days": true,
      "handle": "string",
      "include_zero_amount": true,
      "interval_length": 1,
      "name": "Ava Chen",
      "partial_period_handling": "string",
      "partial_proration_days": true,
      "prepaid": true,
      "quantity": 1,
      "schedule_type": "string",
      "state": "string",
      "vat": 1,
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `amount_incl_vat` | boolean |  |
| `created` | date |  |
| `currency` | string |  |
| `deleted` | date |  |
| `dunning_plan` | string |  |
| `effective_setup_fee_amount_incl_vat` | boolean |  |
| `effective_setup_fee_vat` | number |  |
| `fixed_trial_days` | boolean |  |
| `handle` | string |  |
| `include_zero_amount` | boolean |  |
| `interval_length` | number |  |
| `name` | string |  |
| `partial_period_handling` | string |  |
| `partial_proration_days` | boolean |  |
| `prepaid` | boolean |  |
| `quantity` | number |  |
| `schedule_type` | string |  |
| `state` | string |  |
| `vat` | number |  |
| `version` | number |  |

## Native endpoint

Through the native Reepay API, this operation is `GET /v1/plan/:handle/current` (base URL `https://api.frisbii.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-plan.md) for the provider-specific parameters and requirements.

