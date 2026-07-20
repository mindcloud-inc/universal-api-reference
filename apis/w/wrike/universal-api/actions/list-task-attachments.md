# Wrike: List Task Attachments

Finds attachments on a Wrike task.

```
GET https://connect.mindcloud.co/v1/universal/wrike/latest/actions/list-task-attachments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wrike `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wrike/latest/actions/list-task-attachments?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wrike/latest/actions/list-task-attachments?${params}`, {
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
| `taskId` | string | yes | Wrike task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorId": "string",
      "commentId": "string",
      "contentType": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "folderId": "string",
      "height": 1,
      "id": "string",
      "name": "Ava Chen",
      "playlistUrl": "https://example.com",
      "previewUrl": "https://example.com",
      "size": 1,
      "taskId": "string",
      "type": "string",
      "url": "https://example.com",
      "version": 1,
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorId` | string |  |
| `commentId` | string |  |
| `contentType` | string |  |
| `createdDate` | date |  |
| `folderId` | string |  |
| `height` | number |  |
| `id` | string |  |
| `name` | string |  |
| `playlistUrl` | string |  |
| `previewUrl` | string |  |
| `size` | number |  |
| `taskId` | string |  |
| `type` | string |  |
| `url` | string |  |
| `version` | number |  |
| `width` | number |  |

## Native endpoint

Through the native Wrike API, this operation is `GET /tasks/:taskId/attachments` (base URL `https://{{credentials.accessTokenRequest.host}}/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-task-attachments.md) for the provider-specific parameters and requirements.

