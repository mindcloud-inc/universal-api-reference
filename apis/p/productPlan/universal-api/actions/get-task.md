# ProductPlan: Get Task

Retrieves a task from ProductPlan.

```
GET https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProductPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-task?connectionId=$CONNECTION_ID&id=string&launchId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "launchId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-task?${params}`, {
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
| `launchId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigned_user_id": 1,
      "checklist_section_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "due_date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "status": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigned_user_id` | number |  |
| `checklist_section_id` | number |  |
| `created_at` | date |  |
| `description` | string |  |
| `due_date` | date |  |
| `id` | number |  |
| `name` | string |  |
| `status` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native ProductPlan API, this operation is `GET /launches/:launch_id/tasks/:id` (base URL `https://app.productplan.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

