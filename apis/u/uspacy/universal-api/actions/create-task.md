# Uspacy: Create Task

Creates a new task in Uspacy.

```
POST https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uspacy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "created_by": 1,
  "setter_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "created_by": 1,
    "setter_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | The task title. |
| `created_by` | number | yes | The user ID that created the task. |
| `setter_id` | string | yes | The user ID who assigned the task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptResult": true,
      "accomplicesIds": [
        "string"
      ],
      "auditorsIds": [
        "string"
      ],
      "basicTask": true,
      "body": "string",
      "createdDate": 1,
      "delegation": true,
      "id": "string",
      "priority": "string",
      "requiredResult": true,
      "status": "string",
      "taskType": "string",
      "template": true,
      "timeEstimate": 1,
      "timeTracking": true,
      "title": "string",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptResult` | boolean |  |
| `accomplicesIds` | array<string> |  |
| `auditorsIds` | array<string> |  |
| `basicTask` | boolean |  |
| `body` | string |  |
| `createdDate` | number |  |
| `delegation` | boolean |  |
| `id` | string |  |
| `priority` | string |  |
| `requiredResult` | boolean |  |
| `status` | string |  |
| `taskType` | string |  |
| `template` | boolean |  |
| `timeEstimate` | number |  |
| `timeTracking` | boolean |  |
| `title` | string |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Uspacy API, this operation is `POST /tasks/v1/tasks` (base URL `https://{{credentials.site}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

