# CloudConvert: Create Job

Creates a job in your CloudConvert account.

```
POST https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/create-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudConvert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/create-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tasks": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/create-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tasks": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tasks` | object | yes | Object containing one or more named CloudConvert tasks. |
| `tag` | string | no | Optional tag to identify the job. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "endedAt": "string",
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "startedAt": "string",
      "status": "string",
      "tag": "string",
      "tasks": [
        {
          "code": "string",
          "copyOfTaskId": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "credits": "string",
          "endedAt": "string",
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
          "result": "string",
          "retryOfTaskId": "string",
          "startedAt": "string",
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
| `endedAt` | string |  |
| `id` | string |  |
| `links.self` | string |  |
| `startedAt` | string |  |
| `status` | string |  |
| `tag` | string |  |
| `tasks[].code` | string |  |
| `tasks[].copyOfTaskId` | string |  |
| `tasks[].createdAt` | date |  |
| `tasks[].credits` | string |  |
| `tasks[].endedAt` | string |  |
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
| `tasks[].result` | string |  |
| `tasks[].retryOfTaskId` | string |  |
| `tasks[].startedAt` | string |  |
| `tasks[].status` | string |  |
| `tasks[].storage` | string |  |
| `tasks[].userId` | number |  |

## Native endpoint

Through the native CloudConvert API, this operation is `POST /jobs` (base URL `https://api.cloudconvert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job.md) for the provider-specific parameters and requirements.

