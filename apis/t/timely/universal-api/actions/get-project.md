# Timely: Get Project

Retrieves a project from Timely.

```
GET https://connect.mindcloud.co/v1/universal/timely/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timely/latest/actions/get-project?connectionId=$CONNECTION_ID&accountId=1&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timely/latest/actions/get-project?${params}`, {
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
| `accountId` | number | yes | Account ID |
| `id` | number | yes | Project ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": 1,
      "active": true,
      "allow_only_one_tag": true,
      "billable": true,
      "billed_cost": {
        "amount": 1,
        "currency_code": "string",
        "formatted": "string",
        "fractional": 1
      },
      "budget": 1,
      "budget_calculation": "string",
      "budget_expired_on": "string",
      "budget_percent": 1,
      "budget_progress": 1,
      "budget_scope": "string",
      "budget_type": "string",
      "client": {},
      "color": "string",
      "cost": {
        "amount": 1,
        "currency_code": "string",
        "formatted": "string",
        "fractional": 1
      },
      "created_at": 1,
      "created_from": "string",
      "currency": {
        "id": "string",
        "iso_code": "string",
        "name": "Ava Chen",
        "symbol": "string",
        "symbol_first": true
      },
      "default_label_ids": [
        1
      ],
      "default_labels": true,
      "description": "string",
      "enable_labels": "string",
      "estimated_cost": {
        "amount": 1,
        "currency_code": "string",
        "formatted": "string",
        "fractional": 1
      },
      "external_id": "string",
      "first_logged_on": "string",
      "has_recurrence": true,
      "hour_rate": 1,
      "hour_rate_in_cents": 1,
      "id": 1,
      "invoice_by_budget": true,
      "label_ids": [
        1
      ],
      "labels": {
        "budget": 1,
        "default": true,
        "label_id": 1,
        "project_id": 1,
        "required": true,
        "updated_at": "2026-05-07T12:00:00.000Z"
      },
      "last_logged_on": "string",
      "locked_hours": true,
      "name": "Ava Chen",
      "rate_type": "string",
      "required_label_ids": [
        1
      ],
      "required_labels": true,
      "required_notes": true,
      "team_ids": [
        1
      ],
      "tic": {
        "external_url": "https://example.com",
        "tool_id": "string",
        "uri": "string"
      },
      "unbilled_cost": {
        "fractional": 1
      },
      "update_hour_billable_state": true,
      "updated_at": 1,
      "users": {
        "created_at": "2026-05-07T12:00:00.000Z",
        "deleted": true,
        "hour_rate": 1,
        "hour_rate_in_cents": 1,
        "internal_hour_rate": 1,
        "internal_hour_rate_in_cents": 1,
        "updated_at": "2026-05-07T12:00:00.000Z",
        "user_id": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | number |  |
| `active` | boolean |  |
| `allow_only_one_tag` | boolean |  |
| `billable` | boolean |  |
| `billed_cost` | object |  |
| `billed_cost.amount` | number |  |
| `billed_cost.currency_code` | string |  |
| `billed_cost.formatted` | string |  |
| `billed_cost.fractional` | number |  |
| `budget` | number |  |
| `budget_calculation` | string |  |
| `budget_expired_on` | string |  |
| `budget_percent` | number |  |
| `budget_progress` | number |  |
| `budget_scope` | string |  |
| `budget_type` | string |  |
| `client` | object |  |
| `color` | string |  |
| `cost` | object |  |
| `cost.amount` | number |  |
| `cost.currency_code` | string |  |
| `cost.formatted` | string |  |
| `cost.fractional` | number |  |
| `created_at` | number |  |
| `created_from` | string |  |
| `currency` | object |  |
| `currency.id` | string |  |
| `currency.iso_code` | string |  |
| `currency.name` | string |  |
| `currency.symbol` | string |  |
| `currency.symbol_first` | boolean |  |
| `default_label_ids` | array<number> |  |
| `default_labels` | boolean |  |
| `description` | string |  |
| `enable_labels` | string |  |
| `estimated_cost` | object |  |
| `estimated_cost.amount` | number |  |
| `estimated_cost.currency_code` | string |  |
| `estimated_cost.formatted` | string |  |
| `estimated_cost.fractional` | number |  |
| `external_id` | string |  |
| `first_logged_on` | string |  |
| `has_recurrence` | boolean |  |
| `hour_rate` | number |  |
| `hour_rate_in_cents` | number |  |
| `id` | number |  |
| `invoice_by_budget` | boolean |  |
| `label_ids` | array<number> |  |
| `labels` | array<object> |  |
| `labels.budget` | number |  |
| `labels.default` | boolean |  |
| `labels.label_id` | number |  |
| `labels.project_id` | number |  |
| `labels.required` | boolean |  |
| `labels.updated_at` | date |  |
| `last_logged_on` | string |  |
| `locked_hours` | boolean |  |
| `name` | string |  |
| `rate_type` | string |  |
| `required_label_ids` | array<number> |  |
| `required_labels` | boolean |  |
| `required_notes` | boolean |  |
| `team_ids` | array<number> |  |
| `tic` | object |  |
| `tic.external_url` | string |  |
| `tic.tool_id` | string |  |
| `tic.uri` | string |  |
| `unbilled_cost` | object |  |
| `unbilled_cost.fractional` | number |  |
| `update_hour_billable_state` | boolean |  |
| `updated_at` | number |  |
| `users` | array<object> |  |
| `users.created_at` | date |  |
| `users.deleted` | boolean |  |
| `users.hour_rate` | number |  |
| `users.hour_rate_in_cents` | number |  |
| `users.internal_hour_rate` | number |  |
| `users.internal_hour_rate_in_cents` | number |  |
| `users.updated_at` | date |  |
| `users.user_id` | number |  |

## Native endpoint

Through the native Timely API, this operation is `GET /1.1/{account_id}/projects/{id}` (base URL `https://api.timelyapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

