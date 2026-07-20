# CoordinateHQ: List Entity



```
GET https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/list-entity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoordinateHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/list-entity?connectionId=$CONNECTION_ID&startDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/list-entity?${params}`, {
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
| `startDate` | string | yes |  |
| `endDate` | string | no |  |
| `entity` | list<string> | no |  |
| `sort` | list<string> | no |  |

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
      "taskDescription": {},
      "taskDueDate": "string",
      "taskGroupTitle": "string",
      "taskId": "string",
      "taskInternal": {},
      "taskStartDate": {},
      "taskStatusCurrent": "string",
      "taskStatusCurrentDt": "string",
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
| `taskDescription` | object |  |
| `taskDueDate` | string |  |
| `taskGroupTitle` | string |  |
| `taskId` | string |  |
| `taskInternal` | object |  |
| `taskStartDate` | object |  |
| `taskStatusCurrent` | string |  |
| `taskStatusCurrentDt` | string |  |
| `taskTitle` | string |  |
| `vendorId` | string |  |

## Native endpoint

Through the native CoordinateHQ API, this operation is `GET /entity` (base URL `https://app.coordinatehq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-entity.md) for the provider-specific parameters and requirements.

