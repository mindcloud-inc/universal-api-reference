# CoordinateHQ: Download Task File



```
GET https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/download-task-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoordinateHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/download-task-file?connectionId=$CONNECTION_ID&project_id=string&task_id=string&file_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "string",
  "task_id": "string",
  "file_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/download-task-file?${params}`, {
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
| `project_id` | string | yes |  |
| `task_id` | string | yes |  |
| `file_id` | string | yes |  |

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
      "groupId": "string",
      "lastModifiedDt": "string",
      "projectExternalObjectId": {},
      "projectId": "string",
      "projectName": "Ava Chen",
      "taskAssigneeStakeholderEmailAddress": {},
      "taskAssigneeStakeholderFullName": {},
      "taskAssigneeStakeholderId": {},
      "taskCompletedByEmail": {},
      "taskCompletedByName": {},
      "taskCompletedDt": {},
      "taskDescription": {},
      "taskDueDate": "string",
      "taskGroupTitle": "string",
      "taskId": "string",
      "taskInternal": {},
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
| `groupId` | string |  |
| `lastModifiedDt` | string |  |
| `projectExternalObjectId` | object |  |
| `projectId` | string |  |
| `projectName` | string |  |
| `taskAssigneeStakeholderEmailAddress` | object |  |
| `taskAssigneeStakeholderFullName` | object |  |
| `taskAssigneeStakeholderId` | object |  |
| `taskCompletedByEmail` | object |  |
| `taskCompletedByName` | object |  |
| `taskCompletedDt` | object |  |
| `taskDescription` | object |  |
| `taskDueDate` | string |  |
| `taskGroupTitle` | string |  |
| `taskId` | string |  |
| `taskInternal` | object |  |
| `taskStartDate` | object |  |
| `taskStatusCurrent` | object |  |
| `taskStatusCurrentDt` | object |  |
| `taskTitle` | string |  |
| `vendorId` | string |  |

## Native endpoint

Through the native CoordinateHQ API, this operation is `GET /projects/:project_id/task/:task_id/file/:file_id` (base URL `https://app.coordinatehq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-task-file.md) for the provider-specific parameters and requirements.

