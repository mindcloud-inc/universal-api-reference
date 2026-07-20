# Frame.io v4: Get Comment

Retrieves a comment from Frame.io v4.

```
GET https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/get-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frame.io v4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/get-comment?connectionId=$CONNECTION_ID&accountId=string&commentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "commentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/get-comment?${params}`, {
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
| `accountId` | string | yes |  |
| `commentId` | string | yes |  |
| `timestampAsTimecode` | boolean | no |  |
| `include` | string | no |  |

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
      "owner": {
        "active": true,
        "adobeUserId": "string",
        "avatarUrl": "https://example.com",
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "page": 1,
      "replies": [
        [
          {}
        ]
      ],
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
| `owner` | object | User details |
| `owner.active` | boolean | User active status |
| `owner.adobeUserId` | string | Adobe user ID |
| `owner.avatarUrl` | string | User avatar image url |
| `owner.email` | string | User email |
| `owner.id` | string | User ID - can be null for invited users with no frame account |
| `owner.name` | string | User name |
| `page` | number | Document page |
| `replies[]` | array<object> | Replies |
| `replies[].annotation` | string |  |
| `replies[].completedAt` | date | Completion timestamp |
| `replies[].completerId` | string | ID of user who marked the comment as completed |
| `replies[].createdAt` | date | Creation timestamp |
| `replies[].fileId` | string | File ID |
| `replies[].id` | string | Comment ID |
| `replies[].page` | number | Document page |
| `replies[].text` | string | Comment text |
| `replies[].textEditedAt` | date | Text edited timestamp |
| `replies[].timestamp` | string | Comment timecode in media. Only allowed when file type is 'audio', 'stream', or 'video'. |
| `replies[].updatedAt` | date | Update timestamp |
| `text` | string | Comment text |
| `textEditedAt` | date | Text edited timestamp |
| `timestamp` | string | Comment timecode in media. Only allowed when file type is 'audio', 'stream', or 'video'. |
| `updatedAt` | date | Update timestamp |

## Native endpoint

Through the native Frame.io v4 API, this operation is `GET /accounts/:accountId/comments/:commentId` (base URL `https://api.frame.io/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-comment.md) for the provider-specific parameters and requirements.

