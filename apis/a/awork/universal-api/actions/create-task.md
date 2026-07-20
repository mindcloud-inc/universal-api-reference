# Awork: Create Task

Creates a task in Awork.

```
POST https://connect.mindcloud.co/v1/universal/awork/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Awork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/awork/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "baseType": "projecttask"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/awork/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "baseType": "projecttask"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the task. |
| `baseType` | string | yes | Use private for a private task or projecttask for a project task. Example: `projecttask`. |
| `entityId` | string | no | Required for project tasks and must be the project ID. Example: `19da7493-7e95-499e-b0c3-3cfba6444bd0`. |
| `description` | string | no | The description of the task. Example: `Created by MindCloud during Awork action validation.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseType": "string",
      "checklistItemsCount": 1,
      "checklistItemsDoneCount": 1,
      "commentCount": 1,
      "correlationId": "string",
      "createdBy": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "createdVia": "string",
      "deriveDatesFromSubtasks": true,
      "description": "string",
      "entityId": "string",
      "hasAttachment": true,
      "id": "string",
      "isCompletelyScheduled": true,
      "isExternal": true,
      "isHiddenForConnectUsers": true,
      "isPrio": true,
      "isRecurring": true,
      "isSubtask": true,
      "laneOrder": 1,
      "name": "Ava Chen",
      "numberOfSubtasks": 1,
      "order": 1,
      "plannedDuration": 1,
      "project": {
        "createdBy": "string",
        "hasImage": true,
        "id": "string",
        "isBillableByDefault": true,
        "isExternal": true,
        "isPrivate": true,
        "members": [
          {
            "id": "string",
            "isExternal": true,
            "isResponsible": true,
            "projectRoleId": "string",
            "projectRoleName": "Ava Chen",
            "userId": "string"
          }
        ],
        "name": "Ava Chen",
        "projectKey": "string",
        "projectStatus": {
          "id": "string",
          "isArchived": true,
          "name": "Ava Chen",
          "type": "string"
        }
      },
      "projectId": "string",
      "resourceVersion": 1,
      "taskIdentifier": "string",
      "taskNumber": 1,
      "taskSchedulesCount": 1,
      "taskStatus": {
        "createdBy": "string",
        "createdOn": "2026-05-07T12:00:00.000Z",
        "icon": "string",
        "id": "string",
        "name": "Ava Chen",
        "order": 1,
        "projectId": "string",
        "type": "string",
        "updatedBy": "string",
        "updatedOn": "2026-05-07T12:00:00.000Z"
      },
      "taskStatusId": "string",
      "totalPlannedDurationWithHierarchy": 1,
      "trackedDuration": 1,
      "typeOfWork": {
        "icon": "string",
        "id": "string",
        "isArchived": true,
        "name": "Ava Chen"
      },
      "typeOfWorkId": "string",
      "updatedBy": "string",
      "updatedOn": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseType` | string |  |
| `checklistItemsCount` | number |  |
| `checklistItemsDoneCount` | number |  |
| `commentCount` | number |  |
| `correlationId` | string |  |
| `createdBy` | string |  |
| `createdOn` | date |  |
| `createdVia` | string |  |
| `deriveDatesFromSubtasks` | boolean |  |
| `description` | string |  |
| `entityId` | string |  |
| `hasAttachment` | boolean |  |
| `id` | string |  |
| `isCompletelyScheduled` | boolean |  |
| `isExternal` | boolean |  |
| `isHiddenForConnectUsers` | boolean |  |
| `isPrio` | boolean |  |
| `isRecurring` | boolean |  |
| `isSubtask` | boolean |  |
| `laneOrder` | number |  |
| `name` | string |  |
| `numberOfSubtasks` | number |  |
| `order` | number |  |
| `plannedDuration` | number |  |
| `project.createdBy` | string |  |
| `project.hasImage` | boolean |  |
| `project.id` | string |  |
| `project.isBillableByDefault` | boolean |  |
| `project.isExternal` | boolean |  |
| `project.isPrivate` | boolean |  |
| `project.members[].id` | string |  |
| `project.members[].isExternal` | boolean |  |
| `project.members[].isResponsible` | boolean |  |
| `project.members[].projectRoleId` | string |  |
| `project.members[].projectRoleName` | string |  |
| `project.members[].userId` | string |  |
| `project.name` | string |  |
| `project.projectKey` | string |  |
| `project.projectStatus.id` | string |  |
| `project.projectStatus.isArchived` | boolean |  |
| `project.projectStatus.name` | string |  |
| `project.projectStatus.type` | string |  |
| `projectId` | string |  |
| `resourceVersion` | number |  |
| `taskIdentifier` | string |  |
| `taskNumber` | number |  |
| `taskSchedulesCount` | number |  |
| `taskStatus.createdBy` | string |  |
| `taskStatus.createdOn` | date |  |
| `taskStatus.icon` | string |  |
| `taskStatus.id` | string |  |
| `taskStatus.name` | string |  |
| `taskStatus.order` | number |  |
| `taskStatus.projectId` | string |  |
| `taskStatus.type` | string |  |
| `taskStatus.updatedBy` | string |  |
| `taskStatus.updatedOn` | date |  |
| `taskStatusId` | string |  |
| `totalPlannedDurationWithHierarchy` | number |  |
| `trackedDuration` | number |  |
| `typeOfWork.icon` | string |  |
| `typeOfWork.id` | string |  |
| `typeOfWork.isArchived` | boolean |  |
| `typeOfWork.name` | string |  |
| `typeOfWorkId` | string |  |
| `updatedBy` | string |  |
| `updatedOn` | date |  |

## Native endpoint

Through the native Awork API, this operation is `POST /tasks` (base URL `https://api.awork.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

