# Kite Suite: Get sprints by project ID



```
GET https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-sprints-by-project-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-sprints-by-project-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-sprints-by-project-id?${params}`, {
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
| `id` | string | no |  |

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

Through the native Kite Suite API, this operation is `GET /api/v1/sprint/project/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sprints-by-project-id.md) for the provider-specific parameters and requirements.

