# Hubflo: Retrieve Task

Retrieves a task from Hubflo by ID.

```
GET https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/retrieve-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hubflo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/retrieve-task?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/retrieve-task?${params}`, {
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
      "clickup_id": "string",
      "completed": true,
      "contact_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "creator_id": "string",
      "creator_type": "string",
      "description": "string",
      "end_time": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "kind": "string",
      "monday_id": "string",
      "name": "Ava Chen",
      "parent_task_id": "string",
      "project_id": "string",
      "project_section_id": "string",
      "slug": "string",
      "start_time": "string",
      "tags": [
        "string"
      ],
      "visible_by_contact": true,
      "workspace_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clickup_id` | string |  |
| `completed` | boolean |  |
| `contact_id` | string |  |
| `created_at` | date |  |
| `creator_id` | string |  |
| `creator_type` | string |  |
| `description` | string |  |
| `end_time` | date |  |
| `id` | string |  |
| `kind` | string |  |
| `monday_id` | string |  |
| `name` | string |  |
| `parent_task_id` | string |  |
| `project_id` | string |  |
| `project_section_id` | string |  |
| `slug` | string |  |
| `start_time` | string |  |
| `tags` | array<string> |  |
| `visible_by_contact` | boolean |  |
| `workspace_id` | string |  |

## Native endpoint

Through the native Hubflo API, this operation is `GET /tasks/:id` (base URL `https://app.hubflo.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-task.md) for the provider-specific parameters and requirements.

