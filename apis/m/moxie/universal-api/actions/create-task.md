# Moxie: Create Task

Creates a new task in Moxie.

```
POST https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moxie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "clientName": "Ava Chen",
  "projectName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "clientName": "Ava Chen",
    "projectName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Task name. |
| `clientName` | string | yes | Existing client name for the task. |
| `projectName` | string | yes | Existing project name for the task. |
| `status` | string | no | Task status label. |
| `description` | string | no | Task description. |
| `dueDate` | date | no | Task due date. |
| `startDate` | date | no | Task start date. |
| `priority` | number | no | Task priority value. |
| `assignedTo` | list<string> | no | List of assignee emails. |
| `tasks` | list<string> | no | Optional list of subtask labels. |
| `customValues` | object | no | Custom values object for the task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "approvalRequired": true,
      "approvals": [
        {}
      ],
      "archived": true,
      "assignedToList": [
        {}
      ],
      "clientId": "string",
      "comments": [
        {}
      ],
      "created": "2026-05-07T12:00:00.000Z",
      "customValues": [
        {}
      ],
      "description": "string",
      "events": [
        {}
      ],
      "files": [
        {}
      ],
      "id": "string",
      "isSubTask": true,
      "name": "Ava Chen",
      "priority": 1,
      "projectId": "string",
      "projectTypeId": "string",
      "sampleData": true,
      "statusId": "string",
      "taskPriority": "string",
      "tasks": [
        {}
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `approvalRequired` | boolean |  |
| `approvals` | array<object> |  |
| `archived` | boolean |  |
| `assignedToList` | array<object> |  |
| `clientId` | string |  |
| `comments` | array<object> |  |
| `created` | date |  |
| `customValues` | array<object> |  |
| `description` | string |  |
| `events` | array<object> |  |
| `files` | array<object> |  |
| `id` | string |  |
| `isSubTask` | boolean |  |
| `name` | string |  |
| `priority` | number |  |
| `projectId` | string |  |
| `projectTypeId` | string |  |
| `sampleData` | boolean |  |
| `statusId` | string |  |
| `taskPriority` | string |  |
| `tasks` | array<object> |  |
| `type` | string |  |

## Native endpoint

Through the native Moxie API, this operation is `POST /action/tasks/create` (base URL `https://pod01.withmoxie.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

