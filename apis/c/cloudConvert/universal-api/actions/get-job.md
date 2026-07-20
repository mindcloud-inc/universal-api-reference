# CloudConvert: Get Job

Retrieves a job from your CloudConvert account.

```
GET https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/get-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudConvert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/get-job?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/get-job?${params}`, {
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
| `id` | string | yes | CloudConvert job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "endedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "startedAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "tag": "string",
      "tasks": [
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
          "name": "Ava Chen",
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `endedAt` | date |  |
| `id` | string |  |
| `links.self` | string |  |
| `startedAt` | date |  |
| `status` | string |  |
| `tag` | string |  |
| `tasks[].code` | string |  |
| `tasks[].copyOfTaskId` | string |  |
| `tasks[].createdAt` | date |  |
| `tasks[].credits` | number |  |
| `tasks[].endedAt` | date |  |
| `tasks[].hostName` | string |  |
| `tasks[].id` | string |  |
| `tasks[].jobId` | string |  |
| `tasks[].links.self` | string |  |
| `tasks[].message` | string |  |
| `tasks[].name` | string |  |
| `tasks[].operation` | string |  |
| `tasks[].percent` | number |  |
| `tasks[].priority` | number |  |
| `tasks[].region` | string |  |
| `tasks[].result.files[].filename` | string |  |
| `tasks[].result.files[].size` | number |  |
| `tasks[].retryOfTaskId` | string |  |
| `tasks[].startedAt` | date |  |
| `tasks[].status` | string |  |
| `tasks[].storage` | string |  |
| `tasks[].userId` | number |  |

## Native endpoint

Through the native CloudConvert API, this operation is `GET /jobs/:id` (base URL `https://api.cloudconvert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job.md) for the provider-specific parameters and requirements.

