# Outlign: Create Task

Creates a new task in Outlign.

```
POST https://connect.mindcloud.co/v1/universal/outlign/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outlign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/outlign/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "phaseId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/outlign/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "phaseId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Task title |
| `phaseId` | number | yes | Phase to attach the task to |
| `dueDate` | string | no | Task due date Example: `2026-04-20`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "client": {
          "id": 1,
          "title": "string"
        },
        "company": {
          "id": 1,
          "title": "string"
        },
        "completed": true,
        "createdAt": "string",
        "dueDate": "string",
        "id": 1,
        "phase": {
          "id": 1,
          "isInternal": true,
          "title": "string"
        },
        "project": {
          "id": 1,
          "title": "string"
        },
        "published": true,
        "title": "string",
        "updatedAt": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.client.id` | number |  |
| `data.client.title` | string |  |
| `data.company.id` | number |  |
| `data.company.title` | string |  |
| `data.completed` | boolean |  |
| `data.createdAt` | string |  |
| `data.dueDate` | string |  |
| `data.id` | number |  |
| `data.phase.id` | number |  |
| `data.phase.isInternal` | boolean |  |
| `data.phase.title` | string |  |
| `data.project.id` | number |  |
| `data.project.title` | string |  |
| `data.published` | boolean |  |
| `data.title` | string |  |
| `data.updatedAt` | string |  |

## Native endpoint

Through the native Outlign API, this operation is `POST /steps` (base URL `https://go.outlign.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

