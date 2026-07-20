# PiAPI/MMAudio: Get Task

Retrieves an MMAudio task from PiAPI/MMAudio.

```
GET https://connect.mindcloud.co/v1/universal/piAPIMMAudio/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/MMAudio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIMMAudio/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=task%20identifier%20returned%20by%20Generate%20Audio" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "task identifier returned by Generate Audio"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIMMAudio/latest/actions/get-task?${params}`, {
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
| `taskId` | string | yes | The PiAPI task_id returned when you create the MMAudio task. Example: `task identifier returned by Generate Audio`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "input": "string",
      "metadata": {
        "createdAt": "string",
        "endedAt": "string",
        "quotaFrozen": 1,
        "quotaUsage": 1,
        "startedAt": "string"
      },
      "status": "string",
      "task": {
        "createTime": 1,
        "deleted": true,
        "favored": true,
        "id": 1,
        "status": 1,
        "type": "string",
        "updateTime": 1,
        "userId": 1
      },
      "taskId": "string",
      "works": [
        {
          "contentType": "string",
          "cover": {
            "resource": "string"
          },
          "deleted": true,
          "publishStatus": "string",
          "resource": {
            "duration": 1,
            "resource": "string",
            "resourceWithoutWatermark": "string"
          },
          "status": 1,
          "workId": 1
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
| `input` | string |  |
| `metadata.createdAt` | string |  |
| `metadata.endedAt` | string |  |
| `metadata.quotaFrozen` | number |  |
| `metadata.quotaUsage` | number |  |
| `metadata.startedAt` | string |  |
| `status` | string |  |
| `task.createTime` | number |  |
| `task.deleted` | boolean |  |
| `task.favored` | boolean |  |
| `task.id` | number |  |
| `task.status` | number |  |
| `task.type` | string |  |
| `task.updateTime` | number |  |
| `task.userId` | number |  |
| `taskId` | string |  |
| `works[].contentType` | string |  |
| `works[].cover.resource` | string |  |
| `works[].deleted` | boolean |  |
| `works[].publishStatus` | string |  |
| `works[].resource.duration` | number |  |
| `works[].resource.resource` | string |  |
| `works[].resource.resourceWithoutWatermark` | string |  |
| `works[].status` | number |  |
| `works[].workId` | number |  |

## Native endpoint

Through the native PiAPI/MMAudio API, this operation is `GET /api/v1/task/{task_id}` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

