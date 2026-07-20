# Float: Create Project Task

Creates a new project task in Float.

```
POST https://connect.mindcloud.co/v1/universal/float/latest/actions/create-project-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Float `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/float/latest/actions/create-project-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "11207922",
  "taskName": "Design"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/float/latest/actions/create-project-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "11207922",
    "taskName": "Design"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `phaseId` | number | no | The ID of the phase the project task belongs to Example: `2063834`. |
| `projectId` | number | yes | The ID of the project the project task belongs to Example: `11207922`. |
| `taskName` | string | yes | The name of the project task Example: `Design`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billable": 1,
      "budget": {},
      "created": "string",
      "modified": "string",
      "phaseId": 1,
      "projectId": 1,
      "taskMetaId": 1,
      "taskName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billable` | number |  |
| `budget` | object |  |
| `created` | string |  |
| `modified` | string |  |
| `phaseId` | number |  |
| `projectId` | number |  |
| `taskMetaId` | number |  |
| `taskName` | string |  |

## Native endpoint

Through the native Float API, this operation is `POST /project-tasks` (base URL `https://api.float.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-task.md) for the provider-specific parameters and requirements.

