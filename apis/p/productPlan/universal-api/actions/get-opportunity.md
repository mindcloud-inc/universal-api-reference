# ProductPlan: Get Opportunity

Retrieves an opportunity from ProductPlan.

```
GET https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProductPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-opportunity?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-opportunity?${params}`, {
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
      "bars_count": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "idea_ids": [
        1
      ],
      "ideas_count": 1,
      "location_status": "string",
      "objective_ids": [
        1
      ],
      "problem_statement": "string",
      "team_ids": [
        1
      ],
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_id": 1,
      "workflow_status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bar_ids` | array<number> |  |
| `bars_count` | number |  |
| `created_at` | date |  |
| `description` | string |  |
| `id` | number |  |
| `idea_ids` | array<number> |  |
| `ideas_count` | number |  |
| `location_status` | string |  |
| `objective_ids` | array<number> |  |
| `problem_statement` | string |  |
| `team_ids` | array<number> |  |
| `updated_at` | date |  |
| `user_id` | number |  |
| `workflow_status` | string |  |

## Native endpoint

Through the native ProductPlan API, this operation is `GET /discovery/opportunities/:id` (base URL `https://app.productplan.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-opportunity.md) for the provider-specific parameters and requirements.

