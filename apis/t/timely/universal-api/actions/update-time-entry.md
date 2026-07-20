# Timely: Update Time Entry

Updates an existing time entry in Timely.

```
PUT https://connect.mindcloud.co/v1/universal/timely/latest/actions/update-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timely/latest/actions/update-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "id": 1,
  "event": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timely/latest/actions/update-time-entry', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "id": 1,
    "event": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | Account ID |
| `id` | number | yes | Time entry ID |
| `event` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billable": true,
      "billed": true,
      "billed_at": "string",
      "cost": {
        "amount": 1,
        "currency_code": "string",
        "formatted": "string",
        "fractional": 1
      },
      "created_at": 1,
      "created_from": "string",
      "creator_id": "string",
      "day": "string",
      "deleted": true,
      "draft": true,
      "duration": {
        "formatted": "string",
        "hours": 1,
        "minutes": 1,
        "seconds": 1,
        "total_hours": 1,
        "total_minutes": 1,
        "total_seconds": 1
      },
      "entry_ids": [
        1
      ],
      "estimated": true,
      "estimated_cost": {
        "amount": 1,
        "currency_code": "string",
        "formatted": "string",
        "fractional": 1
      },
      "estimated_duration": {
        "formatted": "string",
        "hours": 1,
        "minutes": 1,
        "seconds": 1,
        "total_hours": 1,
        "total_minutes": 1,
        "total_seconds": 1
      },
      "estimated_internal_cost": {
        "amount": 1,
        "currency_code": "string",
        "formatted": "string",
        "fractional": 1
      },
      "external_id": "string",
      "external_link_ids": [
        1
      ],
      "forecast_id": "string",
      "from": "string",
      "hour_rate": 1,
      "hour_rate_in_cents": 1,
      "id": 1,
      "internal_cost": {
        "amount": 1,
        "currency_code": "string",
        "formatted": "string",
        "fractional": 1
      },
      "internal_cost_rate": 1,
      "invoice_id": "string",
      "label_ids": [
        1
      ],
      "locked": true,
      "locked_reason": "string",
      "manage": true,
      "note": "string",
      "profit": 1,
      "profitability": 1,
      "project": {},
      "sequence": 1,
      "suggestion_id": "string",
      "timer_started_on": 1,
      "timer_state": "string",
      "timer_stopped_on": 1,
      "timestamps": {
        "from": "string",
        "hour_id": 1,
        "id": 1
      },
      "to": "string",
      "uid": "string",
      "updated_at": 1,
      "updated_from": "string",
      "updater_id": "string",
      "user": {},
      "user_ids": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billable` | boolean |  |
| `billed` | boolean |  |
| `billed_at` | string |  |
| `cost` | object |  |
| `cost.amount` | number |  |
| `cost.currency_code` | string |  |
| `cost.formatted` | string |  |
| `cost.fractional` | number |  |
| `created_at` | number |  |
| `created_from` | string |  |
| `creator_id` | string |  |
| `day` | string |  |
| `deleted` | boolean |  |
| `draft` | boolean |  |
| `duration` | object |  |
| `duration.formatted` | string |  |
| `duration.hours` | number |  |
| `duration.minutes` | number |  |
| `duration.seconds` | number |  |
| `duration.total_hours` | number |  |
| `duration.total_minutes` | number |  |
| `duration.total_seconds` | number |  |
| `entry_ids` | array<number> |  |
| `estimated` | boolean |  |
| `estimated_cost` | object |  |
| `estimated_cost.amount` | number |  |
| `estimated_cost.currency_code` | string |  |
| `estimated_cost.formatted` | string |  |
| `estimated_cost.fractional` | number |  |
| `estimated_duration` | object |  |
| `estimated_duration.formatted` | string |  |
| `estimated_duration.hours` | number |  |
| `estimated_duration.minutes` | number |  |
| `estimated_duration.seconds` | number |  |
| `estimated_duration.total_hours` | number |  |
| `estimated_duration.total_minutes` | number |  |
| `estimated_duration.total_seconds` | number |  |
| `estimated_internal_cost` | object |  |
| `estimated_internal_cost.amount` | number |  |
| `estimated_internal_cost.currency_code` | string |  |
| `estimated_internal_cost.formatted` | string |  |
| `estimated_internal_cost.fractional` | number |  |
| `external_id` | string |  |
| `external_link_ids` | array<number> |  |
| `forecast_id` | string |  |
| `from` | string |  |
| `hour_rate` | number |  |
| `hour_rate_in_cents` | number |  |
| `id` | number |  |
| `internal_cost` | object |  |
| `internal_cost_rate` | number |  |
| `internal_cost.amount` | number |  |
| `internal_cost.currency_code` | string |  |
| `internal_cost.formatted` | string |  |
| `internal_cost.fractional` | number |  |
| `invoice_id` | string |  |
| `label_ids` | array<number> |  |
| `locked` | boolean |  |
| `locked_reason` | string |  |
| `manage` | boolean |  |
| `note` | string |  |
| `profit` | number |  |
| `profitability` | number |  |
| `project` | object |  |
| `sequence` | number |  |
| `suggestion_id` | string |  |
| `timer_started_on` | number |  |
| `timer_state` | string |  |
| `timer_stopped_on` | number |  |
| `timestamps` | array<object> |  |
| `timestamps.from` | string |  |
| `timestamps.hour_id` | number |  |
| `timestamps.id` | number |  |
| `to` | string |  |
| `uid` | string |  |
| `updated_at` | number |  |
| `updated_from` | string |  |
| `updater_id` | string |  |
| `user` | object |  |
| `user_ids` | array<number> |  |

## Native endpoint

Through the native Timely API, this operation is `PUT /1.1/{account_id}/hours/{id}` (base URL `https://api.timelyapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-time-entry.md) for the provider-specific parameters and requirements.

