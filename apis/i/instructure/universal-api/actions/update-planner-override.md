# Instructure: Update Planner Override

Updates an existing planner override in Instructure Canvas.

```
PUT https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-planner-override
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-planner-override" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-planner-override', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dismissed` | string | no | Whether the plannable item is dismissed. |
| `id` | string | yes | The Canvas planner override ID. |
| `markedComplete` | string | no | Whether the plannable item is marked complete. |

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

Through the native Instructure API, this operation is `PUT /planner/overrides/:id` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-planner-override.md) for the provider-specific parameters and requirements.

