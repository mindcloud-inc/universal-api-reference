# Instructure: Get Planner Override

Retrieves a planner override from Instructure Canvas.

```
GET https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-planner-override
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-planner-override?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-planner-override?${params}`, {
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
| `id` | string | yes | The Canvas planner override ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignment_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "dismissed": true,
      "id": 1,
      "marked_complete": true,
      "plannable_id": 1,
      "plannable_type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_id": 1,
      "workflow_state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignment_id` | number |  |
| `created_at` | date |  |
| `deleted_at` | date |  |
| `dismissed` | boolean |  |
| `id` | number |  |
| `marked_complete` | boolean |  |
| `plannable_id` | number |  |
| `plannable_type` | string |  |
| `updated_at` | date |  |
| `user_id` | number |  |
| `workflow_state` | string |  |

## Native endpoint

Through the native Instructure API, this operation is `GET /planner/overrides/:id` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-planner-override.md) for the provider-specific parameters and requirements.

