# Float: Update Project

Updates an existing project in Float.

```
PUT https://connect.mindcloud.co/v1/universal/float/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Float `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/float/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "11207922"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/float/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "11207922"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `notes` | string | no | Notes for this project Example: `Updated by MindCloud`. |
| `projectId` | number | yes | The project's ID Example: `11207922`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": 1,
      "allPmsSchedule": 1,
      "budgetPerPhase": 1,
      "budgetPriority": 1,
      "budgetTotal": {},
      "budgetType": 1,
      "clientId": 1,
      "color": "string",
      "created": "string",
      "defaultHourlyRate": {},
      "endDate": "string",
      "lockedTaskList": 1,
      "modified": "string",
      "name": "Ava Chen",
      "nonBillable": 1,
      "notes": "string",
      "projectCode": {},
      "projectId": 1,
      "projectManager": 1,
      "stageId": 1,
      "startDate": "string",
      "status": 1,
      "tentative": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | number |  |
| `allPmsSchedule` | number |  |
| `budgetPerPhase` | number |  |
| `budgetPriority` | number |  |
| `budgetTotal` | object |  |
| `budgetType` | number |  |
| `clientId` | number |  |
| `color` | string |  |
| `created` | string |  |
| `defaultHourlyRate` | object |  |
| `endDate` | string |  |
| `lockedTaskList` | number |  |
| `modified` | string |  |
| `name` | string |  |
| `nonBillable` | number |  |
| `notes` | string |  |
| `projectCode` | object |  |
| `projectId` | number |  |
| `projectManager` | number |  |
| `stageId` | number |  |
| `startDate` | string |  |
| `status` | number |  |
| `tentative` | number |  |

## Native endpoint

Through the native Float API, this operation is `PATCH /projects/:project_id` (base URL `https://api.float.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

