# Instructure: Update Planner Note

Updates an existing planner note in Instructure Canvas.

```
PUT https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-planner-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-planner-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-planner-note', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `details` | string | no | Details for the planner note. |
| `id` | string | yes | The Canvas planner note ID. |
| `title` | string | yes | The title of the planner note. |
| `todoDate` | string | no | The date and time for the planner note. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "course_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "details": "string",
      "id": 1,
      "title": "string",
      "todo_date": "2026-05-07T12:00:00.000Z",
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
| `course_id` | number |  |
| `created_at` | date |  |
| `details` | string |  |
| `id` | number |  |
| `title` | string |  |
| `todo_date` | date |  |
| `updated_at` | date |  |
| `user_id` | number |  |
| `workflow_state` | string |  |

## Native endpoint

Through the native Instructure API, this operation is `PUT /planner_notes/:id` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-planner-note.md) for the provider-specific parameters and requirements.

