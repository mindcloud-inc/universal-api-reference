# CoordinateHQ: Get Task



```
GET https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoordinateHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/get-task?connectionId=$CONNECTION_ID&task_id=string&project_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "task_id": "string",
  "project_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/get-task?${params}`, {
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
| `task_id` | string | yes |  |
| `project_id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customers": [
        {
          "customerId": "string",
          "customerName": "Ava Chen"
        }
      ],
      "entityType": "string",
      "entityUrl": "https://example.com",
      "externalObjectId": {},
      "files": [
        {
          "downloadUrl": "https://example.com",
          "fileContentType": "string",
          "fileDt": "string",
          "fileName": "Ava Chen",
          "fileSize": 1,
          "fileUid": "string"
        }
      ],
      "groupId": "string",
      "lastModifiedDt": "string",
      "projectExternalObjectId": {},
      "projectId": "string",
      "projectName": "Ava Chen",
      "taskAssigneeStakeholderEmailAddress": "ava@example.com",
      "taskAssigneeStakeholderFullName": "Ava Chen",
      "taskAssigneeStakeholderId": "string",
      "taskAssignments": [
        {
          "stakeholderAssignmentDt": "string",
          "stakeholderEmailAddress": "ava@example.com",
          "stakeholderFullName": "Ava Chen",
          "stakeholderId": "string"
        }
      ],
      "taskCompletedByEmail": {},
      "taskCompletedByName": {},
      "taskCompletedDt": {},
      "taskDescription": "string",
      "taskDueDate": {},
      "taskGroupTitle": "string",
      "taskId": "string",
      "taskInternal": true,
      "taskSortOrder": {},
      "taskStartDate": {},
      "taskStatusCurrent": {},
      "taskStatusCurrentDt": {},
      "taskTitle": "string",
      "vendorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customers[].customerId` | string |  |
| `customers[].customerName` | string |  |
| `entityType` | string |  |
| `entityUrl` | string |  |
| `externalObjectId` | object |  |
| `files[].downloadUrl` | string |  |
| `files[].fileContentType` | string |  |
| `files[].fileDt` | string |  |
| `files[].fileName` | string |  |
| `files[].fileSize` | number |  |
| `files[].fileUid` | string |  |
| `groupId` | string |  |
| `lastModifiedDt` | string |  |
| `projectExternalObjectId` | object |  |
| `projectId` | string |  |
| `projectName` | string |  |
| `taskAssigneeStakeholderEmailAddress` | string |  |
| `taskAssigneeStakeholderFullName` | string |  |
| `taskAssigneeStakeholderId` | string |  |
| `taskAssignments[].stakeholderAssignmentDt` | string |  |
| `taskAssignments[].stakeholderEmailAddress` | string |  |
| `taskAssignments[].stakeholderFullName` | string |  |
| `taskAssignments[].stakeholderId` | string |  |
| `taskCompletedByEmail` | object |  |
| `taskCompletedByName` | object |  |
| `taskCompletedDt` | object |  |
| `taskDescription` | string |  |
| `taskDueDate` | object |  |
| `taskGroupTitle` | string |  |
| `taskId` | string |  |
| `taskInternal` | boolean |  |
| `taskSortOrder` | object |  |
| `taskStartDate` | object |  |
| `taskStatusCurrent` | object |  |
| `taskStatusCurrentDt` | object |  |
| `taskTitle` | string |  |
| `vendorId` | string |  |

## Native endpoint

Through the native CoordinateHQ API, this operation is `GET /projects/:project_id/task/:task_id` (base URL `https://app.coordinatehq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

