# Zoho Projects: List Tasks By Project

Retrieves tasks from a Zoho Projects project.

```
GET https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/list-tasks-by-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Projects `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/list-tasks-by-project?connectionId=$CONNECTION_ID&limit=25&offset=0&portalId=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "portalId": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/list-tasks-by-project?${params}`, {
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
| `sortBy` | string | no | Task sort expression. |
| `viewId` | string | no | Custom view ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | string | no | Raw JSON filter object from Zoho Projects. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pageInfo": {
        "hasNextPage": true,
        "page": 1,
        "pageCount": 1,
        "perPage": 1
      },
      "tasks": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pageInfo.hasNextPage` | boolean |  |
| `pageInfo.page` | number |  |
| `pageInfo.pageCount` | number |  |
| `pageInfo.perPage` | number |  |
| `tasks[]` | array<object> |  |
| `tasks[].associationInfo.hasAttachments` | boolean |  |
| `tasks[].associationInfo.hasComments` | boolean |  |
| `tasks[].associationInfo.hasForums` | boolean |  |
| `tasks[].associationInfo.hasRecurrence` | boolean |  |
| `tasks[].associationInfo.hasReminder` | boolean |  |
| `tasks[].associationInfo.hasSubtasks` | boolean |  |
| `tasks[].billingType` | string |  |
| `tasks[].completionPercentage` | number |  |
| `tasks[].createdBy.email` | string |  |
| `tasks[].createdBy.firstName` | string |  |
| `tasks[].createdBy.lastName` | string |  |
| `tasks[].createdBy.name` | string |  |
| `tasks[].createdBy.zpuid` | string |  |
| `tasks[].createdBy.zuid` | number |  |
| `tasks[].createdTime` | date |  |
| `tasks[].createdVia` | string |  |
| `tasks[].depth` | number |  |
| `tasks[].duration.type` | string |  |
| `tasks[].duration.value` | string |  |
| `tasks[].endDate` | date |  |
| `tasks[].id` | string |  |
| `tasks[].isCompleted` | boolean |  |
| `tasks[].lastModifiedTime` | date |  |
| `tasks[].logHours.billableHours` | string |  |
| `tasks[].logHours.nonBillableHours` | string |  |
| `tasks[].logHours.totalHours` | string |  |
| `tasks[].milestone.id` | string |  |
| `tasks[].milestone.name` | string |  |
| `tasks[].name` | string |  |
| `tasks[].ownersAndWork.copyTaskDuration` | boolean |  |
| `tasks[].ownersAndWork.owners[]` | array<object> |  |
| `tasks[].ownersAndWork.owners[].email` | string |  |
| `tasks[].ownersAndWork.owners[].firstName` | string |  |
| `tasks[].ownersAndWork.owners[].lastName` | string |  |
| `tasks[].ownersAndWork.owners[].name` | string |  |
| `tasks[].ownersAndWork.owners[].workValues` | string |  |
| `tasks[].ownersAndWork.owners[].zpuid` | string |  |
| `tasks[].ownersAndWork.owners[].zuid` | number |  |
| `tasks[].ownersAndWork.refreshBusinessHours` | boolean |  |
| `tasks[].ownersAndWork.totalWork` | string |  |
| `tasks[].ownersAndWork.unit` | string |  |
| `tasks[].ownersAndWork.workType` | string |  |
| `tasks[].prefix` | string |  |
| `tasks[].priority` | string |  |
| `tasks[].project.id` | string |  |
| `tasks[].project.name` | string |  |
| `tasks[].sequence.sequence` | number |  |
| `tasks[].startDate` | date |  |
| `tasks[].status.color` | string |  |
| `tasks[].status.colorHexcode` | string |  |
| `tasks[].status.id` | string |  |
| `tasks[].status.isClosedType` | boolean |  |
| `tasks[].status.name` | string |  |
| `tasks[].tasklist.id` | string |  |
| `tasks[].tasklist.name` | string |  |
| `tasks[].updatedBy.email` | string |  |
| `tasks[].updatedBy.firstName` | string |  |
| `tasks[].updatedBy.lastName` | string |  |
| `tasks[].updatedBy.name` | string |  |
| `tasks[].updatedBy.zpuid` | string |  |
| `tasks[].updatedBy.zuid` | number |  |

## Native endpoint

Through the native Zoho Projects API, this operation is `GET /portal/[:PORTALID]/projects/[:PROJECTID]/tasks` (base URL `https://projectsapi.zoho.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks-by-project.md) for the provider-specific parameters and requirements.

