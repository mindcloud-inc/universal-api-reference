# Zoho Projects: Update Task

Updates an existing task in Zoho Projects.

```
PUT https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Projects `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "portalId": "string",
  "projectId": "string",
  "taskId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "portalId": "string",
    "projectId": "string",
    "taskId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `portalId` | string | yes | Zoho Projects portal ID. |
| `projectId` | string | yes | Zoho Projects project ID. |
| `taskId` | string | yes | Zoho Projects task ID. |
| `name` | string | no | Task name. |
| `description` | string | no | Task description. |
| `tasklist.id` | string | no | Task list ID. |
| `parentalInfo.parentTaskId` | string | no | Parent task ID for subtask updates. |
| `status.id` | string | no | Task status ID. |
| `priority` | string | no | Task priority. |
| `startDate` | string | no | Task start date. |
| `endDate` | string | no | Task end date. |
| `duration.value` | string | no | Task duration value. |
| `duration.type` | string | no | Task duration unit. |
| `completionPercentage` | number | no | Task completion percentage. |
| `billingType` | string | no | Task billing type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "associationInfo": {
        "hasAttachments": true,
        "hasComments": true,
        "hasForums": true,
        "hasRecurrence": true,
        "hasReminder": true,
        "hasSubtasks": true
      },
      "billingType": "string",
      "completionPercentage": 1,
      "createdBy": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "name": "Ava Chen",
        "zpuid": "string",
        "zuid": 1
      },
      "createdTime": "2026-05-07T12:00:00.000Z",
      "createdVia": "string",
      "depth": 1,
      "duration": {
        "type": "string",
        "value": "string"
      },
      "endDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isCompleted": true,
      "lastModifiedTime": "2026-05-07T12:00:00.000Z",
      "logHours": {
        "billableHours": "string",
        "nonBillableHours": "string",
        "totalHours": "string"
      },
      "milestone": {
        "id": "string",
        "name": "Ava Chen"
      },
      "name": "Ava Chen",
      "ownersAndWork": {
        "copyTaskDuration": true,
        "owners": [
          [
            {}
          ]
        ],
        "refreshBusinessHours": true,
        "totalWork": "string",
        "unit": "string",
        "workType": "string"
      },
      "prefix": "string",
      "priority": "string",
      "project": {
        "id": "string",
        "name": "Ava Chen"
      },
      "sequence": {
        "sequence": 1
      },
      "startDate": "2026-05-07T12:00:00.000Z",
      "status": {
        "color": "string",
        "colorHexcode": "string",
        "id": "string",
        "isClosedType": true,
        "name": "Ava Chen"
      },
      "tasklist": {
        "id": "string",
        "name": "Ava Chen"
      },
      "updatedBy": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "name": "Ava Chen",
        "zpuid": "string",
        "zuid": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `associationInfo.hasAttachments` | boolean |  |
| `associationInfo.hasComments` | boolean |  |
| `associationInfo.hasForums` | boolean |  |
| `associationInfo.hasRecurrence` | boolean |  |
| `associationInfo.hasReminder` | boolean |  |
| `associationInfo.hasSubtasks` | boolean |  |
| `billingType` | string |  |
| `completionPercentage` | number |  |
| `createdBy.email` | string |  |
| `createdBy.firstName` | string |  |
| `createdBy.lastName` | string |  |
| `createdBy.name` | string |  |
| `createdBy.zpuid` | string |  |
| `createdBy.zuid` | number |  |
| `createdTime` | date |  |
| `createdVia` | string |  |
| `depth` | number |  |
| `duration.type` | string |  |
| `duration.value` | string |  |
| `endDate` | date |  |
| `id` | string |  |
| `isCompleted` | boolean |  |
| `lastModifiedTime` | date |  |
| `logHours.billableHours` | string |  |
| `logHours.nonBillableHours` | string |  |
| `logHours.totalHours` | string |  |
| `milestone.id` | string |  |
| `milestone.name` | string |  |
| `name` | string |  |
| `ownersAndWork.copyTaskDuration` | boolean |  |
| `ownersAndWork.owners[]` | array<object> |  |
| `ownersAndWork.owners[].email` | string |  |
| `ownersAndWork.owners[].firstName` | string |  |
| `ownersAndWork.owners[].lastName` | string |  |
| `ownersAndWork.owners[].name` | string |  |
| `ownersAndWork.owners[].workValues` | string |  |
| `ownersAndWork.owners[].zpuid` | string |  |
| `ownersAndWork.owners[].zuid` | number |  |
| `ownersAndWork.refreshBusinessHours` | boolean |  |
| `ownersAndWork.totalWork` | string |  |
| `ownersAndWork.unit` | string |  |
| `ownersAndWork.workType` | string |  |
| `prefix` | string |  |
| `priority` | string |  |
| `project.id` | string |  |
| `project.name` | string |  |
| `sequence.sequence` | number |  |
| `startDate` | date |  |
| `status.color` | string |  |
| `status.colorHexcode` | string |  |
| `status.id` | string |  |
| `status.isClosedType` | boolean |  |
| `status.name` | string |  |
| `tasklist.id` | string |  |
| `tasklist.name` | string |  |
| `updatedBy.email` | string |  |
| `updatedBy.firstName` | string |  |
| `updatedBy.lastName` | string |  |
| `updatedBy.name` | string |  |
| `updatedBy.zpuid` | string |  |
| `updatedBy.zuid` | number |  |

## Native endpoint

Through the native Zoho Projects API, this operation is `PATCH /portal/[:PORTALID]/projects/[:PROJECTID]/tasks/[:TASKID]` (base URL `https://projectsapi.zoho.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

