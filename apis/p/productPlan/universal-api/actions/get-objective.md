# ProductPlan: Get Objective

Retrieves an objective from ProductPlan.

```
GET https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-objective
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProductPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-objective?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-objective?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bar_ids": [
        1
      ],
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "end_date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "key_result_ids": [
        1
      ],
      "location_status": "string",
      "name": "Ava Chen",
      "opportunity_ids": [
        1
      ],
      "risk_status": "string",
      "start_date": "2026-05-07T12:00:00.000Z",
      "subject": "string",
      "team_ids": [
        1
      ],
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bar_ids` | array<number> |  |
| `created_at` | date |  |
| `description` | string |  |
| `end_date` | date |  |
| `id` | number |  |
| `key_result_ids` | array<number> |  |
| `location_status` | string |  |
| `name` | string |  |
| `opportunity_ids` | array<number> |  |
| `risk_status` | string |  |
| `start_date` | date |  |
| `subject` | string |  |
| `team_ids` | array<number> |  |
| `updated_at` | date |  |

## Native endpoint

Through the native ProductPlan API, this operation is `GET /strategy/objectives/:id` (base URL `https://app.productplan.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-objective.md) for the provider-specific parameters and requirements.

