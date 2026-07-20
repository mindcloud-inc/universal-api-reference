# Hubflo: Update Task

Updates an existing task in Hubflo.

```
PUT https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hubflo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `name` | string | yes |  |
| `description` | string | no |  |
| `startTime` | string | no |  |
| `completed` | boolean | no |  |
| `clickupId` | string | no |  |
| `mondayId` | string | no |  |
| `kind` | string | no |  |
| `visibleByContact` | boolean | no |  |
| `projectId` | string | no |  |
| `projectSectionId` | string | no |  |
| `contactId` | string | no |  |
| `workspaceId` | string | no |  |
| `userIds` | list<string> | no |  |
| `contactIds` | list<string> | no |  |
| `tags` | list<string> | no |  |

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
      "end_time": "string",
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
| `end_time` | string |  |
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

Through the native Hubflo API, this operation is `PATCH /tasks/:id` (base URL `https://app.hubflo.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

