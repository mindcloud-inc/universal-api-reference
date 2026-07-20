# Manus: Get Task

Retrieves a task from Manus by ID.

```
GET https://connect.mindcloud.co/v1/universal/manus/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Manus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/manus/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/manus/latest/actions/get-task?${params}`, {
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
| `taskId` | string | yes | The ID of the task to retrieve |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `convert` | boolean | no | Whether to convert the task result to a structured response |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "creditUsage": 1,
      "id": "string",
      "metadata": {
        "taskTitle": "string",
        "taskUrl": "https://example.com"
      },
      "model": "string",
      "object": "string",
      "output": [
        {
          "content": [
            {
              "text": "string",
              "type": "string"
            }
          ],
          "id": "string",
          "role": "string",
          "status": "string",
          "type": "string"
        }
      ],
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `creditUsage` | number |  |
| `id` | string |  |
| `metadata.taskTitle` | string |  |
| `metadata.taskUrl` | string |  |
| `model` | string |  |
| `object` | string |  |
| `output[].content[].text` | string |  |
| `output[].content[].type` | string |  |
| `output[].id` | string |  |
| `output[].role` | string |  |
| `output[].status` | string |  |
| `output[].type` | string |  |
| `status` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Manus API, this operation is `GET /tasks/:task_id` (base URL `https://api.manus.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

