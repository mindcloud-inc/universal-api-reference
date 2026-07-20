# Zoho Projects: Get Task Details

Retrieves task details from Zoho Projects.

```
GET https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/get-task-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Projects `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/get-task-details?connectionId=$CONNECTION_ID&portalId=string&projectId=string&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalId": "string",
  "projectId": "string",
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/get-task-details?${params}`, {
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
| `portalId` | string | yes | Zoho Projects portal ID. |
| `projectId` | string | yes | Zoho Projects project ID. |
| `taskId` | string | yes | Zoho Projects task ID. |

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

Through the native Zoho Projects API, this operation is `GET /portal/[:PORTALID]/projects/[:PROJECTID]/tasks/[:TASKID]` (base URL `https://projectsapi.zoho.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task-details.md) for the provider-specific parameters and requirements.

