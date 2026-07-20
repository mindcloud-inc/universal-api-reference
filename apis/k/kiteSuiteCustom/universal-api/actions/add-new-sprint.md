# Kite Suite: Add New Sprint



```
POST https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/add-new-sprint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/add-new-sprint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "sprintName": "Ava Chen",
  "startDate": "string",
  "project": "string",
  "endDate": "string",
  "duration": "string",
  "sprintGoal": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/add-new-sprint', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "sprintName": "Ava Chen",
    "startDate": "string",
    "project": "string",
    "endDate": "string",
    "duration": "string",
    "sprintGoal": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |
| `sprintName` | string | yes |  |
| `startDate` | string | yes |  |
| `project` | string | yes |  |
| `endDate` | string | yes |  |
| `duration` | string | yes |  |
| `sprintGoal` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": "string",
      "duration": 1,
      "endDate": "string",
      "id": "string",
      "project": {},
      "sprintGoal": "string",
      "sprintName": "Ava Chen",
      "startDate": "string",
      "tasks": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | string | Sprint creator User ID |
| `duration` | number | Duration of sprint(in week) |
| `endDate` | string | End Date of sprint |
| `id` | string | The auto-generated id of the sprint. |
| `project` | object |  |
| `sprintGoal` | string | Sprint Goal. |
| `sprintName` | string | Name of sprint |
| `startDate` | string | Start Date of sprint |
| `tasks` | array |  |

## Native endpoint

Through the native Kite Suite API, this operation is `POST /api/v1/sprint` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-new-sprint.md) for the provider-specific parameters and requirements.

