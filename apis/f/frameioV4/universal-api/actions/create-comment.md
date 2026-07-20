# Frame.io v4: Create Comment

Creates a new comment in Frame.io v4.

```
POST https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/create-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frame.io v4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/create-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "fileId": "string",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/create-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "fileId": "string",
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes |  |
| `fileId` | string | yes |  |
| `timestampAsTimecode` | boolean | no |  |
| `data` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "annotation": "string",
      "completedAt": "2026-05-07T12:00:00.000Z",
      "completerId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fileId": "string",
      "id": "string",
      "page": 1,
      "text": "string",
      "textEditedAt": "2026-05-07T12:00:00.000Z",
      "timestamp": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `annotation` | string |  |
| `completedAt` | date | Completion timestamp |
| `completerId` | string | ID of user who marked the comment as completed |
| `createdAt` | date | Creation timestamp |
| `fileId` | string | File ID |
| `id` | string | Comment ID |
| `page` | number | Document page |
| `text` | string | Comment text |
| `textEditedAt` | date | Text edited timestamp |
| `timestamp` | string | Comment timecode in media. Only allowed when file type is 'audio', 'stream', or 'video'. |
| `updatedAt` | date | Update timestamp |

## Native endpoint

Through the native Frame.io v4 API, this operation is `POST /accounts/:accountId/files/:fileId/comments` (base URL `https://api.frame.io/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-comment.md) for the provider-specific parameters and requirements.

