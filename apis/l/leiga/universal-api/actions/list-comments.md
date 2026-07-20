# Leiga: List Comments

Retrieves comments from Leiga for an issue.

```
GET https://connect.mindcloud.co/v1/universal/leiga/latest/actions/list-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leiga `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leiga/latest/actions/list-comments?connectionId=$CONNECTION_ID&commentModule=string&linkId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "commentModule": "string",
  "linkId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leiga/latest/actions/list-comments?${params}`, {
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
| `commentModule` | string | yes | Comment Module (.eg. issue) |
| `linkId` | number | yes | Link ID |
| `pageNumber` | number | no | Page Number |
| `pageSize` | number | no | Page Size |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commentAttributes": {},
      "commentId": 1,
      "commentNo": 1,
      "commentUser": {},
      "content": "string",
      "createTime": 1,
      "files": [
        {}
      ],
      "plainContent": "string",
      "stickerVOList": [
        {}
      ],
      "subReplies": [
        {}
      ],
      "updateTime": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commentAttributes` | object | Comment metadata. |
| `commentId` | number | Comment ID. |
| `commentNo` | number | Comment count. |
| `commentUser` | object | Comment author. |
| `content` | string | Rendered comment content. |
| `createTime` | number | Creation timestamp. |
| `files` | array<object> | Attached files. |
| `plainContent` | string | Plain comment content. |
| `stickerVOList` | array<object> | Sticker entries. |
| `subReplies` | array<object> | Reply comments. |
| `updateTime` | number | Last update timestamp. |

## Native endpoint

Through the native Leiga API, this operation is `POST /comment/page` (base URL `https://app.leiga.com/openapi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-comments.md) for the provider-specific parameters and requirements.

