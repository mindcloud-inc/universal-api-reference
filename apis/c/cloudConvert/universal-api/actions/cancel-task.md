# CloudConvert: Cancel Task

Cancels a task in your CloudConvert account.

```
PUT https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/cancel-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudConvert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/cancel-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/cancel-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | CloudConvert task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "copyOfTaskId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "credits": 1,
      "endedAt": "2026-05-07T12:00:00.000Z",
      "hostName": "Ava Chen",
      "id": "string",
      "jobId": "string",
      "links": {
        "self": "https://example.com"
      },
      "message": "string",
      "operation": "string",
      "percent": 1,
      "priority": 1,
      "region": "string",
      "result": {
        "form": {
          "parameters": {
            "acl": "string",
            "key": "string",
            "policy": "string",
            "successActionStatus": "string",
            "xAmzAlgorithm": "string",
            "xAmzCredential": "string",
            "xAmzDate": "string",
            "xAmzSignature": "string"
          },
          "url": "https://example.com"
        }
      },
      "retryOfTaskId": "string",
      "startedAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "storage": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `copyOfTaskId` | string |  |
| `createdAt` | date |  |
| `credits` | number |  |
| `endedAt` | date |  |
| `hostName` | string |  |
| `id` | string |  |
| `jobId` | string |  |
| `links.self` | string |  |
| `message` | string |  |
| `operation` | string |  |
| `percent` | number |  |
| `priority` | number |  |
| `region` | string |  |
| `result.form.parameters.acl` | string |  |
| `result.form.parameters.key` | string |  |
| `result.form.parameters.policy` | string |  |
| `result.form.parameters.successActionStatus` | string |  |
| `result.form.parameters.xAmzAlgorithm` | string |  |
| `result.form.parameters.xAmzCredential` | string |  |
| `result.form.parameters.xAmzDate` | string |  |
| `result.form.parameters.xAmzSignature` | string |  |
| `result.form.url` | string |  |
| `retryOfTaskId` | string |  |
| `startedAt` | date |  |
| `status` | string |  |
| `storage` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native CloudConvert API, this operation is `POST /tasks/:id/cancel` (base URL `https://api.cloudconvert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-task.md) for the provider-specific parameters and requirements.

