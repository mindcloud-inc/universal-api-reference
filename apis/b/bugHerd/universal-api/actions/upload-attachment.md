# BugHerd: Upload Attachment

Uploads an attachment to a BugHerd task.

```
POST https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/upload-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BugHerd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/upload-attachment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "511891",
  "task_id": "29003679",
  "file_name": "sample.txt"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/upload-attachment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": "511891",
    "task_id": "29003679",
    "file_name": "sample.txt"
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
| `file_name` | string | yes | Example: `sample.txt`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fileName": "Ava Chen",
      "id": 1,
      "taskId": 1,
      "url": "https://example.com",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `fileName` | string |  |
| `id` | number |  |
| `taskId` | number |  |
| `url` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native BugHerd API, this operation is `POST projects/:project_id/tasks/:task_id/attachments/upload` (base URL `https://www.bugherd.com/api_v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-attachment.md) for the provider-specific parameters and requirements.

