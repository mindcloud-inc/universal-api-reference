# SWELLEnterprise: Create Task

Creates a new task in SWELLEnterprise.

```
POST https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SWELLEnterprise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "statusId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "statusId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | The task title. |
| `projectId` | number | no | The project ID. |
| `statusId` | number | yes | The status ID. |
| `description` | string | no | The task description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "id": 1,
        "project": {
          "id": 1,
          "name": "Ava Chen"
        },
        "statusId": 1,
        "title": "string"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.id` | number | The task ID. |
| `data.project.id` | number | The project ID. |
| `data.project.name` | string | The project name. |
| `data.statusId` | number | The status ID. |
| `data.title` | string | The task title. |
| `message` | string | Success message. |

## Native endpoint

Through the native SWELLEnterprise API, this operation is `POST /projects/tasks` (base URL `https://dashboard.swellsystem.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

