# CloudConvert: Get Task

Retrieves a task from your CloudConvert account.

```
GET https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudConvert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/get-task?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/get-task?${params}`, {
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
        "files": [
          {
            "filename": "Ava Chen",
            "size": 1
          }
        ]
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
| `result.files[].filename` | string |  |
| `result.files[].size` | number |  |
| `retryOfTaskId` | string |  |
| `startedAt` | date |  |
| `status` | string |  |
| `storage` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native CloudConvert API, this operation is `GET /tasks/:id` (base URL `https://api.cloudconvert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

