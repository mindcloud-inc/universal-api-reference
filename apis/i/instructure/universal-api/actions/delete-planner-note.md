# Instructure: Delete Planner Note

Deletes a planner note from Instructure Canvas.

```
DELETE https://connect.mindcloud.co/v1/universal/instructure/latest/actions/delete-planner-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/delete-planner-note?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/delete-planner-note?${params}`, {
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
| `id` | string | yes | The Canvas planner note ID. |

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

Through the native Instructure API, this operation is `DELETE /planner_notes/:id` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-planner-note.md) for the provider-specific parameters and requirements.

