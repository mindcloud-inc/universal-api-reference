# Baremetrics: Create Plan

Creates a plan in Baremetrics.

```
POST https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/create-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Baremetrics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/create-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceId": "source_1",
  "oid": "resource_1",
  "name": "Example Name",
  "currency": "USD",
  "amount": 1,
  "interval": "string",
  "intervalCount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/create-plan', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceId": "source_1",
    "oid": "resource_1",
    "name": "Example Name",
    "currency": "USD",
    "amount": 1,
    "interval": "string",
    "intervalCount": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceId` | string | yes | Please see [Sources](ref:sources) Example: `source_1`. |
| `oid` | string | yes | Your unique ID for the plan Example: `resource_1`. |
| `name` | string | yes | Your internal name for this plan. This will be displayed in the Plan Breakout section Example: `Example Name`. |
| `currency` | string | yes | The ISO code of the currency of this plan. E.G: usd Example: `USD`. |
| `amount` | number | yes | How much is this plan? (In cents) |
| `interval` | string | yes | day, month or year |
| `intervalCount` | number | yes |  |
| `trialDuration` | number | no | The duration of this trial. This is to be used in conjunction with trial_duration_unit |
| `trialDurationUnit` | string | no | This is to be used in conjunction with trial_duration |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Baremetrics API returns.

## Native endpoint

Through the native Baremetrics API, this operation is `POST /v1/:source_id/plans` (base URL `https://sandbox.baremetrics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-plan.md) for the provider-specific parameters and requirements.

