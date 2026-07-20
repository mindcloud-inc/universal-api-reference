# BugHerd: Create Attachment From URL

Creates a task attachment from a URL in BugHerd.

```
POST https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/create-attachment-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BugHerd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/create-attachment-from-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "511891",
  "task_id": "29003679",
  "attachment.file_name": "sample.png",
  "attachment.url": "https://httpbin.org/image/png"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/create-attachment-from-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": "511891",
    "task_id": "29003679",
    "attachment.file_name": "sample.png",
    "attachment.url": "https://httpbin.org/image/png"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project_id` | number | yes | Example: `511891`. |
| `task_id` | number | yes | Example: `29003679`. |
| `attachment` | object | no |  |
| `attachment.file_name` | string | yes | Example: `sample.png`. |
| `attachment.url` | string | yes | Example: `https://httpbin.org/image/png`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "fileName": "Ava Chen",
      "id": 1,
      "taskId": 1,
      "url": "https://example.com",
      "userId": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `fileName` | string |  |
| `id` | number |  |
| `taskId` | number |  |
| `url` | string |  |
| `userId` | object |  |

## Native endpoint

Through the native BugHerd API, this operation is `POST projects/:project_id/tasks/:task_id/attachments.json` (base URL `https://www.bugherd.com/api_v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-attachment-from-url.md) for the provider-specific parameters and requirements.

