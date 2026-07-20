# Timely: Get Report Totals

Retrieves report totals from Timely.

```
GET https://connect.mindcloud.co/v1/universal/timely/latest/actions/get-report-totals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timely/latest/actions/get-report-totals?connectionId=$CONNECTION_ID&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timely/latest/actions/get-report-totals?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `since` | date | no | Start date for the report period (ISO 8601 format: YYYY-MM-DD) |
| `until` | date | no | End date for the report period (ISO 8601 format: YYYY-MM-DD) |
| `userIds` | string | no | Comma-separated list of user IDs to filter by |
| `projectIds` | string | no | Comma-separated list of project IDs to filter by |
| `clientIds` | string | no | Comma-separated list of client IDs to filter by |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billable_duration": {
        "formatted": "string",
        "hours": 1,
        "minutes": 1,
        "seconds": 1,
        "total_hours": 1,
        "total_minutes": 1,
        "total_seconds": 1
      },
      "billed_cost": {
        "amount": 1,
        "currency_code": "string",
        "formatted": "string",
        "fractional": 1
      },
      "billed_duration": {
        "formatted": "string",
        "hours": 1,
        "minutes": 1,
        "seconds": 1,
        "total_hours": 1,
        "total_minutes": 1,
        "total_seconds": 1
      },
      "cost": {
        "amount": 1,
        "currency_code": "string",
        "formatted": "string",
        "fractional": 1
      },
      "duration": {
        "formatted": "string",
        "hours": 1,
        "minutes": 1,
        "seconds": 1,
        "total_hours": 1,
        "total_minutes": 1,
        "total_seconds": 1
      },
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
      "id": 1,
      "internal_cost": {
        "amount": 1,
        "currency_code": "string",
        "formatted": "string",
        "fractional": 1
      },
      "name": "Ava Chen",
      "non_billable_duration": {
        "formatted": "string",
        "hours": 1,
        "minutes": 1,
        "seconds": 1,
        "total_hours": 1,
        "total_minutes": 1,
        "total_seconds": 1
      },
      "profit": {
        "amount": 1,
        "formatted": "string",
        "fractional": 1
      },
      "projects": [
        "string"
      ],
      "unbilled_cost": {
        "amount": 1,
        "currency_code": "string",
        "formatted": "string",
        "fractional": 1
      },
      "unbilled_duration": {
        "formatted": "string",
        "hours": 1,
        "minutes": 1,
        "seconds": 1,
        "total_hours": 1,
        "total_minutes": 1,
        "total_seconds": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billable_duration` | object |  |
| `billable_duration.formatted` | string |  |
| `billable_duration.hours` | number |  |
| `billable_duration.minutes` | number |  |
| `billable_duration.seconds` | number |  |
| `billable_duration.total_hours` | number |  |
| `billable_duration.total_minutes` | number |  |
| `billable_duration.total_seconds` | number |  |
| `billed_cost` | object |  |
| `billed_cost.amount` | number |  |
| `billed_cost.currency_code` | string |  |
| `billed_cost.formatted` | string |  |
| `billed_cost.fractional` | number |  |
| `billed_duration` | object |  |
| `billed_duration.formatted` | string |  |
| `billed_duration.hours` | number |  |
| `billed_duration.minutes` | number |  |
| `billed_duration.seconds` | number |  |
| `billed_duration.total_hours` | number |  |
| `billed_duration.total_minutes` | number |  |
| `billed_duration.total_seconds` | number |  |
| `cost` | object |  |
| `cost.amount` | number |  |
| `cost.currency_code` | string |  |
| `cost.formatted` | string |  |
| `cost.fractional` | number |  |
| `duration` | object |  |
| `duration.formatted` | string |  |
| `duration.hours` | number |  |
| `duration.minutes` | number |  |
| `duration.seconds` | number |  |
| `duration.total_hours` | number |  |
| `duration.total_minutes` | number |  |
| `duration.total_seconds` | number |  |
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
| `id` | number |  |
| `internal_cost` | object |  |
| `internal_cost.amount` | number |  |
| `internal_cost.currency_code` | string |  |
| `internal_cost.formatted` | string |  |
| `internal_cost.fractional` | number |  |
| `name` | string |  |
| `non_billable_duration` | object |  |
| `non_billable_duration.formatted` | string |  |
| `non_billable_duration.hours` | number |  |
| `non_billable_duration.minutes` | number |  |
| `non_billable_duration.seconds` | number |  |
| `non_billable_duration.total_hours` | number |  |
| `non_billable_duration.total_minutes` | number |  |
| `non_billable_duration.total_seconds` | number |  |
| `profit` | object |  |
| `profit.amount` | number |  |
| `profit.formatted` | string |  |
| `profit.fractional` | number |  |
| `projects` | array<string> |  |
| `unbilled_cost` | object |  |
| `unbilled_cost.amount` | number |  |
| `unbilled_cost.currency_code` | string |  |
| `unbilled_cost.formatted` | string |  |
| `unbilled_cost.fractional` | number |  |
| `unbilled_duration` | object |  |
| `unbilled_duration.formatted` | string |  |
| `unbilled_duration.hours` | number |  |
| `unbilled_duration.minutes` | number |  |
| `unbilled_duration.seconds` | number |  |
| `unbilled_duration.total_hours` | number |  |
| `unbilled_duration.total_minutes` | number |  |
| `unbilled_duration.total_seconds` | number |  |

## Native endpoint

Through the native Timely API, this operation is `GET /1.1/{account_id}/reports` (base URL `https://api.timelyapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-report-totals.md) for the provider-specific parameters and requirements.

