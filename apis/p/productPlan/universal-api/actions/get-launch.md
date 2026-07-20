# ProductPlan: Get Launch

Retrieves a launch from ProductPlan.

```
GET https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-launch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProductPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-launch?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-launch?${params}`, {
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
      "checklist_section_ids": [
        1
      ],
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "launch_date": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "progress": 1,
      "status": "string",
      "task_ids": [
        1
      ],
      "team_ids": [
        1
      ],
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bar_ids` | array<number> |  |
| `checklist_section_ids` | array<number> |  |
| `created_at` | date |  |
| `description` | string |  |
| `id` | number |  |
| `launch_date` | date |  |
| `name` | string |  |
| `progress` | number |  |
| `status` | string |  |
| `task_ids` | array<number> |  |
| `team_ids` | array<number> |  |
| `updated_at` | date |  |
| `user_id` | number |  |

## Native endpoint

Through the native ProductPlan API, this operation is `GET /launches/:id` (base URL `https://app.productplan.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-launch.md) for the provider-specific parameters and requirements.

