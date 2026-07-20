# Reepay: List Plans

Retrieves plans from Reepay.

```
GET https://connect.mindcloud.co/v1/universal/reepay/latest/actions/list-plans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reepay `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reepay/latest/actions/list-plans?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reepay/latest/actions/list-plans?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "amount_incl_vat": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "dunning_plan": "string",
      "effective_setup_fee_amount_incl_vat": 1,
      "effective_setup_fee_vat": 1,
      "fixed_trial_days": 1,
      "handle": "string",
      "include_zero_amount": true,
      "interval_length": 1,
      "name": "Ava Chen",
      "partial_period_handling": "string",
      "partial_proration_days": 1,
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
| `amount_incl_vat` | number |  |
| `created` | date |  |
| `currency` | string |  |
| `dunning_plan` | string |  |
| `effective_setup_fee_amount_incl_vat` | number |  |
| `effective_setup_fee_vat` | number |  |
| `fixed_trial_days` | number |  |
| `handle` | string |  |
| `include_zero_amount` | boolean |  |
| `interval_length` | number |  |
| `name` | string |  |
| `partial_period_handling` | string |  |
| `partial_proration_days` | number |  |
| `prepaid` | boolean |  |
| `quantity` | number |  |
| `schedule_type` | string |  |
| `state` | string |  |
| `vat` | number |  |
| `version` | number |  |

## Native endpoint

Through the native Reepay API, this operation is `GET /v1/list/plan` (base URL `https://api.frisbii.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-plans.md) for the provider-specific parameters and requirements.

