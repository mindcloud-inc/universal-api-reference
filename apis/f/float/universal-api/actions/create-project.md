# Float: Create Project

Creates a new project in Float.

```
POST https://connect.mindcloud.co/v1/universal/float/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Float `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/float/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MindCloud Float Project"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/float/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MindCloud Float Project"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | number | no | The ID of the project's client Example: `18400163`. |
| `name` | string | yes | The name of the project Example: `MindCloud Float Project`. |

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
      "endDate": {},
      "lockedTaskList": 1,
      "modified": "string",
      "name": "Ava Chen",
      "nonBillable": 1,
      "notes": {},
      "projectCode": {},
      "projectId": 1,
      "projectManager": 1,
      "stageId": 1,
      "startDate": {},
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
| `endDate` | object |  |
| `lockedTaskList` | number |  |
| `modified` | string |  |
| `name` | string |  |
| `nonBillable` | number |  |
| `notes` | object |  |
| `projectCode` | object |  |
| `projectId` | number |  |
| `projectManager` | number |  |
| `stageId` | number |  |
| `startDate` | object |  |
| `status` | number |  |
| `tentative` | number |  |

## Native endpoint

Through the native Float API, this operation is `POST /projects` (base URL `https://api.float.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

