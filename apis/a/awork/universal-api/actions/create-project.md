# Awork: Create Project

Creates a project in Awork.

```
POST https://connect.mindcloud.co/v1/universal/awork/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Awork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/awork/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MindCloud API project validation 2026-03-20"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/awork/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MindCloud API project validation 2026-03-20"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the project. Example: `MindCloud API project validation 2026-03-20`. |
| `description` | string | no | The project description. Example: `Created by MindCloud during Awork action validation.`. |
| `isPrivate` | boolean | no | Whether the project is private. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | string | no | The id of the company linked to the project. Example: `mkprqomdmlhq`. |

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
      "hasImage": true,
      "id": "string",
      "isBillableByDefault": true,
      "isExternal": true,
      "isMultiAssignmentAllowed": true,
      "isPrivate": true,
      "isRetainer": true,
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
| `hasImage` | boolean |  |
| `id` | string |  |
| `isBillableByDefault` | boolean |  |
| `isExternal` | boolean |  |
| `isMultiAssignmentAllowed` | boolean |  |
| `isPrivate` | boolean |  |
| `isRetainer` | boolean |  |
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
| `tasksCount` | number |  |
| `tasksDoneCount` | number |  |
| `timeBudget` | number |  |
| `totalPlannedDurationWithHierarchy` | number |  |
| `trackedDuration` | number |  |
| `updatedBy` | string |  |
| `updatedOn` | date |  |

## Native endpoint

Through the native Awork API, this operation is `POST /projects` (base URL `https://api.awork.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

