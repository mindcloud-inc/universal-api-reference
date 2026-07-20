# Morningmate: Update Task Status

Updates a task status in Morningmate.

```
PUT https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/update-task-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Morningmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/update-task-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "taskId": 1,
  "registerId": "string",
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/update-task-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "taskId": 1,
    "registerId": "string",
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes |  |
| `taskId` | number | yes |  |
| `registerId` | string | yes |  |
| `status` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": {
        "code": 1,
        "message": "string",
        "success": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | object | Morningmate status-update confirmation envelope. |
| `response.code` | number | Provider confirmation code. |
| `response.message` | string | Provider confirmation message. |
| `response.success` | boolean | Whether Morningmate accepted the task status update. |

## Native endpoint

Through the native Morningmate API, this operation is `PATCH /v1/posts/projects/[:projectId]/tasks/[:taskId]/status` (base URL `https://api.morningmate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task-status.md) for the provider-specific parameters and requirements.

