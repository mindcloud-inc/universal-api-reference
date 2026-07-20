# Float: Get Project

Retrieves project details from Float.

```
GET https://connect.mindcloud.co/v1/universal/float/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Float `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/float/latest/actions/get-project?connectionId=$CONNECTION_ID&projectId=11207922" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "11207922"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/float/latest/actions/get-project?${params}`, {
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
      "calculatedEndDate": "string",
      "calculatedStartDate": "string",
      "clientId": 1,
      "color": "string",
      "created": "string",
      "defaultHourlyRate": {},
      "endDate": "string",
      "lockedTaskList": 1,
      "modified": "string",
      "name": "Ava Chen",
      "nonBillable": 1,
      "notes": {},
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
| `calculatedEndDate` | string |  |
| `calculatedStartDate` | string |  |
| `clientId` | number |  |
| `color` | string |  |
| `created` | string |  |
| `defaultHourlyRate` | object |  |
| `endDate` | string |  |
| `lockedTaskList` | number |  |
| `modified` | string |  |
| `name` | string |  |
| `nonBillable` | number |  |
| `notes` | object |  |
| `projectCode` | object |  |
| `projectId` | number |  |
| `projectManager` | number |  |
| `stageId` | number |  |
| `startDate` | string |  |
| `status` | number |  |
| `tentative` | number |  |

## Native endpoint

Through the native Float API, this operation is `GET /projects/:project_id` (base URL `https://api.float.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

