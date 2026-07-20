# ProjectManager: Retrieve Task

Retrieves a task from ProjectManager.

```
GET https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/retrieve-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProjectManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/retrieve-task?connectionId=$CONNECTION_ID&taskId=22222222-2222-2222-2222-222222222222" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "22222222-2222-2222-2222-222222222222"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/retrieve-task?${params}`, {
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
| `taskId` | string | yes | The unique identifier or short ID of the Task to retrieve Example: `22222222-2222-2222-2222-222222222222`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actualCost": 1,
      "actualDuration": 1,
      "actualEffort": 1,
      "actualFinishDate": "string",
      "actualResourceCost": 1,
      "actualStartDate": "string",
      "approvalLastReminderDate": "string",
      "approvalStatus": "string",
      "approvalStatusModifiedBy": "string",
      "approvalStatusModifiedDate": "string",
      "assignees": {
        "allocatedEffort": 1,
        "avatarUrl": "https://example.com",
        "color": "string",
        "description": "string",
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string",
        "initials": "string",
        "isActive": true,
        "lastName": "Chen",
        "name": "Ava Chen",
        "shortName": "Ava Chen"
      },
      "childTaskCount": 1,
      "color": "string",
      "createDate": "string",
      "description": "string",
      "discussionData": {
        "count": 1,
        "lastReadDate": "string",
        "lastUpdatedDate": "string"
      },
      "fields": {
        "createdDate": "string",
        "id": "string",
        "modifiedDate": "string",
        "name": "Ava Chen",
        "shortId": "string",
        "task": {
          "id": "string",
          "name": "Ava Chen",
          "shortId": "string"
        },
        "type": "string",
        "value": "string"
      },
      "fieldValues": {
        "createdDate": "string",
        "id": "string",
        "modifiedDate": "string",
        "name": "Ava Chen",
        "shortId": "string",
        "task": {
          "id": "string",
          "name": "Ava Chen",
          "shortId": "string"
        },
        "type": "string",
        "value": "string"
      },
      "fileData": {
        "count": 1,
        "lastReadDate": "string",
        "lastUpdatedDate": "string"
      },
      "files": {
        "id": "string",
        "name": "Ava Chen",
        "url": "https://example.com"
      },
      "id": "string",
      "index": 1,
      "isLocked": true,
      "isMilestone": true,
      "isSummary": true,
      "level": 1,
      "modifyDate": "string",
      "name": "Ava Chen",
      "owner": {
        "avatarUrl": "https://example.com",
        "color": "string",
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string",
        "initials": "string",
        "isActive": true,
        "lastName": "Chen"
      },
      "ownerId": "string",
      "parentTaskId": "string",
      "parentTaskName": "Ava Chen",
      "percentComplete": 1,
      "plannedCost": 1,
      "plannedDuration": 1,
      "plannedEffort": 1,
      "plannedFinishDate": "string",
      "plannedResourceCost": 1,
      "plannedStartDate": "string",
      "predecessors": {
        "predecessorId": "string",
        "successorId": "string"
      },
      "priorityId": 1,
      "project": {
        "id": "string",
        "name": "Ava Chen",
        "shortId": "string"
      },
      "projectId": "string",
      "recurring": true,
      "recurringParentTaskId": "string",
      "recurringSettings": {
        "endsAfter": 1,
        "endsOn": "string",
        "repeatEvery": 1,
        "repeatOn": [
          1
        ],
        "repeatOn2Level": 1,
        "type": 1
      },
      "shortId": "string",
      "status": {
        "id": "string",
        "isDone": true,
        "name": "Ava Chen",
        "order": 1,
        "projectId": "string"
      },
      "successors": {
        "predecessorId": "string",
        "successorId": "string"
      },
      "tags": {
        "color": "string",
        "id": "string",
        "name": "Ava Chen"
      },
      "theme": "string",
      "todos": {
        "complete": true,
        "createDate": "string",
        "id": "string",
        "modifyDate": "string",
        "text": "string"
      },
      "wbs": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actualCost` | number |  |
| `actualDuration` | number |  |
| `actualEffort` | number |  |
| `actualFinishDate` | string |  |
| `actualResourceCost` | number |  |
| `actualStartDate` | string |  |
| `approvalLastReminderDate` | string |  |
| `approvalStatus` | string |  |
| `approvalStatusModifiedBy` | string |  |
| `approvalStatusModifiedDate` | string |  |
| `assignees.allocatedEffort` | number |  |
| `assignees.avatarUrl` | string |  |
| `assignees.color` | string |  |
| `assignees.description` | string |  |
| `assignees.email` | string |  |
| `assignees.firstName` | string |  |
| `assignees.id` | string |  |
| `assignees.initials` | string |  |
| `assignees.isActive` | boolean |  |
| `assignees.lastName` | string |  |
| `assignees.name` | string |  |
| `assignees.shortName` | string |  |
| `childTaskCount` | number |  |
| `color` | string |  |
| `createDate` | string |  |
| `description` | string |  |
| `discussionData.count` | number |  |
| `discussionData.lastReadDate` | string |  |
| `discussionData.lastUpdatedDate` | string |  |
| `fields.createdDate` | string |  |
| `fields.id` | string |  |
| `fields.modifiedDate` | string |  |
| `fields.name` | string |  |
| `fields.shortId` | string |  |
| `fields.task.id` | string |  |
| `fields.task.name` | string |  |
| `fields.task.shortId` | string |  |
| `fields.type` | string |  |
| `fields.value` | string |  |
| `fieldValues.createdDate` | string |  |
| `fieldValues.id` | string |  |
| `fieldValues.modifiedDate` | string |  |
| `fieldValues.name` | string |  |
| `fieldValues.shortId` | string |  |
| `fieldValues.task.id` | string |  |
| `fieldValues.task.name` | string |  |
| `fieldValues.task.shortId` | string |  |
| `fieldValues.type` | string |  |
| `fieldValues.value` | string |  |
| `fileData.count` | number |  |
| `fileData.lastReadDate` | string |  |
| `fileData.lastUpdatedDate` | string |  |
| `files.id` | string |  |
| `files.name` | string |  |
| `files.url` | string |  |
| `id` | string |  |
| `index` | number |  |
| `isLocked` | boolean |  |
| `isMilestone` | boolean |  |
| `isSummary` | boolean |  |
| `level` | number |  |
| `modifyDate` | string |  |
| `name` | string |  |
| `owner.avatarUrl` | string |  |
| `owner.color` | string |  |
| `owner.email` | string |  |
| `owner.firstName` | string |  |
| `owner.id` | string |  |
| `owner.initials` | string |  |
| `owner.isActive` | boolean |  |
| `owner.lastName` | string |  |
| `ownerId` | string |  |
| `parentTaskId` | string |  |
| `parentTaskName` | string |  |
| `percentComplete` | number |  |
| `plannedCost` | number |  |
| `plannedDuration` | number |  |
| `plannedEffort` | number |  |
| `plannedFinishDate` | string |  |
| `plannedResourceCost` | number |  |
| `plannedStartDate` | string |  |
| `predecessors.predecessorId` | string |  |
| `predecessors.successorId` | string |  |
| `priorityId` | number |  |
| `project.id` | string |  |
| `project.name` | string |  |
| `project.shortId` | string |  |
| `projectId` | string |  |
| `recurring` | boolean |  |
| `recurringParentTaskId` | string |  |
| `recurringSettings.endsAfter` | number |  |
| `recurringSettings.endsOn` | string |  |
| `recurringSettings.repeatEvery` | number |  |
| `recurringSettings.repeatOn` | array<number> |  |
| `recurringSettings.repeatOn2Level` | number |  |
| `recurringSettings.type` | number |  |
| `shortId` | string |  |
| `status.id` | string |  |
| `status.isDone` | boolean |  |
| `status.name` | string |  |
| `status.order` | number |  |
| `status.projectId` | string |  |
| `successors.predecessorId` | string |  |
| `successors.successorId` | string |  |
| `tags.color` | string |  |
| `tags.id` | string |  |
| `tags.name` | string |  |
| `theme` | string |  |
| `todos.complete` | boolean |  |
| `todos.createDate` | string |  |
| `todos.id` | string |  |
| `todos.modifyDate` | string |  |
| `todos.text` | string |  |
| `wbs` | string |  |

## Native endpoint

Through the native ProjectManager API, this operation is `GET /api/data/tasks/:taskId` (base URL `https://api.projectmanager.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-task.md) for the provider-specific parameters and requirements.

