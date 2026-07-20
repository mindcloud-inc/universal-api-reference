# Uspacy: Get Task

Retrieves a task record from Uspacy.

```
GET https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uspacy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/get-task?${params}`, {
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

Through the native Uspacy API, this operation is `GET /tasks/v1/tasks/:taskId` (base URL `https://{{credentials.site}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

