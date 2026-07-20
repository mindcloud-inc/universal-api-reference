# Grand Avenue Software: Get Equipment Activity Entity Schedule

Retrieves an equipment activity entity schedule from Grand Avenue Software by ID.

```
GET https://connect.mindcloud.co/v1/universal/grandAvenueSoftware/latest/actions/get-equipment-activity-entity-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grand Avenue Software `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grandAvenueSoftware/latest/actions/get-equipment-activity-entity-schedule?connectionId=$CONNECTION_ID&id=123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grandAvenueSoftware/latest/actions/get-equipment-activity-entity-schedule?${params}`, {
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
| `select` | list<string> | no | Accepts multiple values in one string. |
| `expand` | list<string> | no | Accepts multiple values in one string. |
| `id` | number | yes | Default: `123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activityCompletedDate": "2026-05-07T12:00:00.000Z",
      "activityOverdue": "string",
      "activityPerformedByUser": {
        "accountType": "string",
        "active": "string",
        "apiVersion": 1,
        "createdDate": "2026-05-07T12:00:00.000Z",
        "departmentDisplay": "string",
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": 1,
        "lastName": "Chen",
        "updatedTimestamp": "2026-05-07T12:00:00.000Z",
        "userID": "string"
      },
      "activityPerformedByUserDisplay": "string",
      "apiVersion": 1,
      "assigneeDisplay": "string",
      "createdDate": "string",
      "description": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "equipmentDescription": "string",
      "equipmentEntity": {
        "apiVersion": 1,
        "createdDate": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "equipmentID": "string",
        "equipmentProfileDisplay": "string",
        "equipmentStatusDefinitionDisplay": "string",
        "equipmentTypeDefinitionDisplay": "string",
        "id": 1,
        "location": "string",
        "manufacturer": "string",
        "modelNumber": "string",
        "serialNumber": "string",
        "updatedTimestamp": "2026-05-07T12:00:00.000Z"
      },
      "equipmentEntityDisplay": "string",
      "equipmentLocation": "string",
      "equipmentManufacturer": "string",
      "equipmentModelNumber": "string",
      "equipmentProfileDisplay": "string",
      "equipmentSerialNumber": "string",
      "equipmentStatusDefinitionDisplay": "string",
      "equipmentTypeDefinitionDisplay": "string",
      "id": 1,
      "name": "Ava Chen",
      "recordClosedTimestamp": "2026-05-07T12:00:00.000Z",
      "results": "string",
      "reviewTaskRequired": "string",
      "schedulingType": "string",
      "status": "string",
      "taskAssignments": [
        {
          "apiVersion": 1,
          "assigneeDisplay": "string",
          "canceled": "string",
          "completedDate": "2026-05-07T12:00:00.000Z",
          "createdDate": "2026-05-07T12:00:00.000Z",
          "departmentDisplay": "string",
          "id": 1,
          "objectDisplayDescription": "string",
          "objectDisplayID": "string",
          "processName": "Ava Chen",
          "reassignedFromAssignmentDisplay": {},
          "reassignedToAssignmentDisplay": {},
          "status": "string",
          "taskComments": {},
          "taskDueDate": "2026-05-07T12:00:00.000Z",
          "taskDueDateChanged": "string",
          "taskInstructions": {},
          "taskName": "Ava Chen",
          "taskOverdue": "string",
          "taskResults": "string",
          "unclaimed": "string",
          "updatedTimestamp": "2026-05-07T12:00:00.000Z"
        }
      ],
      "type": "string",
      "updatedTimestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activityCompletedDate` | date |  |
| `activityOverdue` | string |  |
| `activityPerformedByUser.accountType` | string |  |
| `activityPerformedByUser.active` | string |  |
| `activityPerformedByUser.apiVersion` | number |  |
| `activityPerformedByUser.createdDate` | date |  |
| `activityPerformedByUser.departmentDisplay` | string |  |
| `activityPerformedByUser.email` | string |  |
| `activityPerformedByUser.firstName` | string |  |
| `activityPerformedByUser.id` | number |  |
| `activityPerformedByUser.lastName` | string |  |
| `activityPerformedByUser.updatedTimestamp` | date |  |
| `activityPerformedByUser.userID` | string |  |
| `activityPerformedByUserDisplay` | string |  |
| `apiVersion` | number |  |
| `assigneeDisplay` | string |  |
| `createdDate` | string |  |
| `description` | string |  |
| `dueDate` | date |  |
| `equipmentDescription` | string |  |
| `equipmentEntity.apiVersion` | number |  |
| `equipmentEntity.createdDate` | date |  |
| `equipmentEntity.description` | string |  |
| `equipmentEntity.equipmentID` | string |  |
| `equipmentEntity.equipmentProfileDisplay` | string |  |
| `equipmentEntity.equipmentStatusDefinitionDisplay` | string |  |
| `equipmentEntity.equipmentTypeDefinitionDisplay` | string |  |
| `equipmentEntity.id` | number |  |
| `equipmentEntity.location` | string |  |
| `equipmentEntity.manufacturer` | string |  |
| `equipmentEntity.modelNumber` | string |  |
| `equipmentEntity.serialNumber` | string |  |
| `equipmentEntity.updatedTimestamp` | date |  |
| `equipmentEntityDisplay` | string |  |
| `equipmentLocation` | string |  |
| `equipmentManufacturer` | string |  |
| `equipmentModelNumber` | string |  |
| `equipmentProfileDisplay` | string |  |
| `equipmentSerialNumber` | string |  |
| `equipmentStatusDefinitionDisplay` | string |  |
| `equipmentTypeDefinitionDisplay` | string |  |
| `id` | number |  |
| `name` | string |  |
| `recordClosedTimestamp` | date |  |
| `results` | string |  |
| `reviewTaskRequired` | string |  |
| `schedulingType` | string |  |
| `status` | string |  |
| `taskAssignments[].apiVersion` | number |  |
| `taskAssignments[].assigneeDisplay` | string |  |
| `taskAssignments[].canceled` | string |  |
| `taskAssignments[].completedDate` | date |  |
| `taskAssignments[].createdDate` | date |  |
| `taskAssignments[].departmentDisplay` | string |  |
| `taskAssignments[].id` | number |  |
| `taskAssignments[].objectDisplayDescription` | string |  |
| `taskAssignments[].objectDisplayID` | string |  |
| `taskAssignments[].processName` | string |  |
| `taskAssignments[].reassignedFromAssignmentDisplay` | object |  |
| `taskAssignments[].reassignedToAssignmentDisplay` | object |  |
| `taskAssignments[].status` | string |  |
| `taskAssignments[].taskComments` | object |  |
| `taskAssignments[].taskDueDate` | date |  |
| `taskAssignments[].taskDueDateChanged` | string |  |
| `taskAssignments[].taskInstructions` | object |  |
| `taskAssignments[].taskName` | string |  |
| `taskAssignments[].taskOverdue` | string |  |
| `taskAssignments[].taskResults` | string |  |
| `taskAssignments[].unclaimed` | string |  |
| `taskAssignments[].updatedTimestamp` | date |  |
| `type` | string |  |
| `updatedTimestamp` | date |  |

## Native endpoint

Through the native Grand Avenue Software API, this operation is `GET /EquipmentEntityActivitySchedules/:id` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-equipment-activity-entity-schedule.md) for the provider-specific parameters and requirements.

