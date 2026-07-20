# Uspacy: Update Task

Updates an existing task in Uspacy.

```
PUT https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uspacy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | The task ID. |

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

Through the native Uspacy API, this operation is `PATCH /tasks/v1/tasks/:taskId` (base URL `https://{{credentials.site}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

