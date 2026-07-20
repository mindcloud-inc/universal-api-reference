# Awork: Create Time Entry

Creates a time entry in Awork using UTC start values.

```
POST https://connect.mindcloud.co/v1/universal/awork/latest/actions/create-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Awork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/awork/latest/actions/create-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "timezone": "UTC",
  "typeOfWorkId": "7de34769-ae34-482f-97ab-295f9660ee2f",
  "userId": "4ac8d1d3-64ca-4db7-b7e5-32226661cd76",
  "startDateUtc": "2026-03-20T00:00:00Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/awork/latest/actions/create-time-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "timezone": "UTC",
    "typeOfWorkId": "7de34769-ae34-482f-97ab-295f9660ee2f",
    "userId": "4ac8d1d3-64ca-4db7-b7e5-32226661cd76",
    "startDateUtc": "2026-03-20T00:00:00Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timezone` | string | yes | The original timezone of the time entry in IANA format. Example: `UTC`. |
| `typeOfWorkId` | string | yes | The id of the type of work. Example: `7de34769-ae34-482f-97ab-295f9660ee2f`. |
| `userId` | string | yes | The id of the user. Example: `4ac8d1d3-64ca-4db7-b7e5-32226661cd76`. |
| `taskId` | string | no | The id of the task. Example: `19e8e816-5618-4e35-a684-e8b2853f9a28`. |
| `startDateUtc` | string | yes | The date in UTC when the time entry was started. Example: `2026-03-20T00:00:00Z`. |
| `startTimeUtc` | string | no | The time in UTC when the time entry was started. Example: `22:30:00`. |
| `duration` | number | no | The duration of the time entry in seconds. Example: `600`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | no | The id of the project. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "duration": 1,
      "endDateLocal": "2026-05-07T12:00:00.000Z",
      "endDateUtc": "2026-05-07T12:00:00.000Z",
      "endTimeLocal": "string",
      "endTimeUtc": "string",
      "id": "string",
      "isBillable": true,
      "isBilled": true,
      "isExternal": true,
      "project": {
        "createdBy": "string",
        "hasImage": true,
        "id": "string",
        "isBillableByDefault": true,
        "isExternal": true,
        "isPrivate": true,
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
      "startDateLocal": "2026-05-07T12:00:00.000Z",
      "startDateUtc": "2026-05-07T12:00:00.000Z",
      "startTimeLocal": "string",
      "startTimeUtc": "string",
      "task": {
        "baseType": "string",
        "correlationId": "string",
        "createdBy": "string",
        "id": "string",
        "lists": [
          {
            "createdBy": "string",
            "createdOn": "2026-05-07T12:00:00.000Z",
            "id": "string",
            "isArchived": true,
            "isHiddenForConnectUsers": true,
            "name": "Ava Chen",
            "order": 1,
            "orderOfTask": 1,
            "plannedDuration": 1,
            "totalPlannedDuration": 1,
            "totalPlannedDurationWithHierarchy": 1,
            "updatedBy": "string",
            "updatedOn": "2026-05-07T12:00:00.000Z"
          }
        ],
        "name": "Ava Chen",
        "plannedDuration": 1,
        "primaryTaskListId": "string",
        "project": {
          "createdBy": "string",
          "hasImage": true,
          "id": "string",
          "isBillableByDefault": true,
          "isExternal": true,
          "isPrivate": true,
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
        "taskIdentifier": "string",
        "taskStatus": {
          "icon": "string",
          "id": "string",
          "name": "Ava Chen",
          "order": 1,
          "type": "string"
        },
        "taskStatusId": "string",
        "totalPlannedDurationWithHierarchy": 1,
        "typeOfWorkId": "string"
      },
      "taskId": "string",
      "timezone": "string",
      "typeOfWork": {
        "icon": "string",
        "id": "string",
        "isArchived": true,
        "name": "Ava Chen"
      },
      "typeOfWorkId": "string",
      "updatedBy": "string",
      "updatedOn": "2026-05-07T12:00:00.000Z",
      "user": {
        "firstName": "Ava",
        "hasImage": true,
        "id": "string",
        "isExternal": true,
        "lastName": "Chen"
      },
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | string |  |
| `createdOn` | date |  |
| `duration` | number |  |
| `endDateLocal` | date |  |
| `endDateUtc` | date |  |
| `endTimeLocal` | string |  |
| `endTimeUtc` | string |  |
| `id` | string |  |
| `isBillable` | boolean |  |
| `isBilled` | boolean |  |
| `isExternal` | boolean |  |
| `project.createdBy` | string |  |
| `project.hasImage` | boolean |  |
| `project.id` | string |  |
| `project.isBillableByDefault` | boolean |  |
| `project.isExternal` | boolean |  |
| `project.isPrivate` | boolean |  |
| `project.name` | string |  |
| `project.projectKey` | string |  |
| `project.projectStatus.id` | string |  |
| `project.projectStatus.isArchived` | boolean |  |
| `project.projectStatus.name` | string |  |
| `project.projectStatus.type` | string |  |
| `projectId` | string |  |
| `resourceVersion` | number |  |
| `startDateLocal` | date |  |
| `startDateUtc` | date |  |
| `startTimeLocal` | string |  |
| `startTimeUtc` | string |  |
| `task.baseType` | string |  |
| `task.correlationId` | string |  |
| `task.createdBy` | string |  |
| `task.id` | string |  |
| `task.lists[].createdBy` | string |  |
| `task.lists[].createdOn` | date |  |
| `task.lists[].id` | string |  |
| `task.lists[].isArchived` | boolean |  |
| `task.lists[].isHiddenForConnectUsers` | boolean |  |
| `task.lists[].name` | string |  |
| `task.lists[].order` | number |  |
| `task.lists[].orderOfTask` | number |  |
| `task.lists[].plannedDuration` | number |  |
| `task.lists[].totalPlannedDuration` | number |  |
| `task.lists[].totalPlannedDurationWithHierarchy` | number |  |
| `task.lists[].updatedBy` | string |  |
| `task.lists[].updatedOn` | date |  |
| `task.name` | string |  |
| `task.plannedDuration` | number |  |
| `task.primaryTaskListId` | string |  |
| `task.project.createdBy` | string |  |
| `task.project.hasImage` | boolean |  |
| `task.project.id` | string |  |
| `task.project.isBillableByDefault` | boolean |  |
| `task.project.isExternal` | boolean |  |
| `task.project.isPrivate` | boolean |  |
| `task.project.name` | string |  |
| `task.project.projectKey` | string |  |
| `task.project.projectStatus.id` | string |  |
| `task.project.projectStatus.isArchived` | boolean |  |
| `task.project.projectStatus.name` | string |  |
| `task.project.projectStatus.type` | string |  |
| `task.projectId` | string |  |
| `task.taskIdentifier` | string |  |
| `task.taskStatus.icon` | string |  |
| `task.taskStatus.id` | string |  |
| `task.taskStatus.name` | string |  |
| `task.taskStatus.order` | number |  |
| `task.taskStatus.type` | string |  |
| `task.taskStatusId` | string |  |
| `task.totalPlannedDurationWithHierarchy` | number |  |
| `task.typeOfWorkId` | string |  |
| `taskId` | string |  |
| `timezone` | string |  |
| `typeOfWork.icon` | string |  |
| `typeOfWork.id` | string |  |
| `typeOfWork.isArchived` | boolean |  |
| `typeOfWork.name` | string |  |
| `typeOfWorkId` | string |  |
| `updatedBy` | string |  |
| `updatedOn` | date |  |
| `user.firstName` | string |  |
| `user.hasImage` | boolean |  |
| `user.id` | string |  |
| `user.isExternal` | boolean |  |
| `user.lastName` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Awork API, this operation is `POST /timeentries` (base URL `https://api.awork.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-time-entry.md) for the provider-specific parameters and requirements.

