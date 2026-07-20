# Awork: List Projects

Retrieves projects from Awork.

```
GET https://connect.mindcloud.co/v1/universal/awork/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Awork `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/awork/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/awork/latest/actions/list-projects?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "deductNonBillableHours": true,
      "description": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "hasImage": true,
      "id": "string",
      "isBillableByDefault": true,
      "isExternal": true,
      "isMultiAssignmentAllowed": true,
      "isPrivate": true,
      "isRetainer": true,
      "members": [
        {
          "firstName": "Ava",
          "hasImage": true,
          "id": "string",
          "isDeactivated": true,
          "isExternal": true,
          "isResponsible": true,
          "lastName": "Chen",
          "projectRoleId": "string",
          "projectRoleName": "Ava Chen",
          "userId": "string"
        }
      ],
      "name": "Ava Chen",
      "plannedDuration": 1,
      "projectKey": "string",
      "projectStatus": {
        "id": "string",
        "isArchived": true,
        "isExternal": true,
        "name": "Ava Chen",
        "type": "string",
        "typeOrder": 1
      },
      "projectStatusId": "string",
      "resourceVersion": 1,
      "startDate": "2026-05-07T12:00:00.000Z",
      "tasksCount": 1,
      "tasksDoneCount": 1,
      "timeBudget": 1,
      "totalPlannedDurationWithHierarchy": 1,
      "trackedDuration": 1,
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
| `createdBy` | string |  |
| `createdOn` | date |  |
| `deductNonBillableHours` | boolean |  |
| `description` | string |  |
| `dueDate` | date |  |
| `hasImage` | boolean |  |
| `id` | string |  |
| `isBillableByDefault` | boolean |  |
| `isExternal` | boolean |  |
| `isMultiAssignmentAllowed` | boolean |  |
| `isPrivate` | boolean |  |
| `isRetainer` | boolean |  |
| `members[].firstName` | string |  |
| `members[].hasImage` | boolean |  |
| `members[].id` | string |  |
| `members[].isDeactivated` | boolean |  |
| `members[].isExternal` | boolean |  |
| `members[].isResponsible` | boolean |  |
| `members[].lastName` | string |  |
| `members[].projectRoleId` | string |  |
| `members[].projectRoleName` | string |  |
| `members[].userId` | string |  |
| `name` | string |  |
| `plannedDuration` | number |  |
| `projectKey` | string |  |
| `projectStatus.id` | string |  |
| `projectStatus.isArchived` | boolean |  |
| `projectStatus.isExternal` | boolean |  |
| `projectStatus.name` | string |  |
| `projectStatus.type` | string |  |
| `projectStatus.typeOrder` | number |  |
| `projectStatusId` | string |  |
| `resourceVersion` | number |  |
| `startDate` | date |  |
| `tasksCount` | number |  |
| `tasksDoneCount` | number |  |
| `timeBudget` | number |  |
| `totalPlannedDurationWithHierarchy` | number |  |
| `trackedDuration` | number |  |
| `updatedBy` | string |  |
| `updatedOn` | date |  |

## Native endpoint

Through the native Awork API, this operation is `GET /projects` (base URL `https://api.awork.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

