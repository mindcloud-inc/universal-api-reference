# Campfire: Retrieve Budget

Retrieves a budget from Campfire.

```
GET https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-budget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campfire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-budget?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-budget?${params}`, {
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
| `id` | number | yes | The budget ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "breakdown_type": "string",
      "cadence": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "customer": 1,
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "department": 1,
      "department_name": "Ava Chen",
      "description": "string",
      "end_date": "2026-05-07T12:00:00.000Z",
      "entity": 1,
      "entity_name": "Ava Chen",
      "id": 1,
      "is_deleted": true,
      "last_modified_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "periods": 1,
      "prior_end_date": "string",
      "prior_start_date": "string",
      "start_date": "2026-05-07T12:00:00.000Z",
      "tags": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `breakdown_type` | string |  |
| `cadence` | string |  |
| `created_at` | date |  |
| `currency` | string |  |
| `customer` | number |  |
| `deleted_at` | date |  |
| `department` | number |  |
| `department_name` | string |  |
| `description` | string |  |
| `end_date` | date |  |
| `entity` | number |  |
| `entity_name` | string |  |
| `id` | number |  |
| `is_deleted` | boolean |  |
| `last_modified_at` | date |  |
| `name` | string |  |
| `periods` | number |  |
| `prior_end_date` | string |  |
| `prior_start_date` | string |  |
| `start_date` | date |  |
| `tags` | array<object> |  |

## Native endpoint

Through the native Campfire API, this operation is `GET /coa/api/budgets/:id` (base URL `https://api.meetcampfire.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-budget.md) for the provider-specific parameters and requirements.

