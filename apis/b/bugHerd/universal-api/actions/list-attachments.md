# BugHerd: List Attachments

Retrieves attachments from a BugHerd task.

```
GET https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/list-attachments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BugHerd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/list-attachments?connectionId=$CONNECTION_ID&projectId=1&taskId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1",
  "taskId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/list-attachments?${params}`, {
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
| `projectId` | number | yes | The BugHerd project ID. |
| `taskId` | number | yes | The BugHerd task ID. |

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
| `createdAt` | date | When the attachment was created. |
| `fileName` | string | The attachment file name, when present. |
| `id` | number | The BugHerd attachment ID. |
| `taskId` | number | The BugHerd task ID that owns the attachment. |
| `url` | string | The attachment URL. |
| `userId` | number | The BugHerd user ID, when present. |

## Native endpoint

Through the native BugHerd API, this operation is `GET projects/:project_id/tasks/:task_id/attachments.json` (base URL `https://www.bugherd.com/api_v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-attachments.md) for the provider-specific parameters and requirements.

