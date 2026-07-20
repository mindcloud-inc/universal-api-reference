# Sleekplan: List Comments



```
GET https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/list-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sleekplan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/list-comments?connectionId=$CONNECTION_ID&limit=25&offset=0&postId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "postId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/list-comments?${params}`, {
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
| `postId` | string | yes |  |
| `sort` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canDelete": true,
      "canEdit": true,
      "comment": "string",
      "commentId": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "feedbackId": 1,
      "likes": 1,
      "productId": 1,
      "status": "string",
      "type": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canDelete` | boolean |  |
| `canEdit` | boolean |  |
| `comment` | string |  |
| `commentId` | number |  |
| `created` | date |  |
| `feedbackId` | number |  |
| `likes` | number |  |
| `productId` | number |  |
| `status` | string |  |
| `type` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Sleekplan API, this operation is `GET /post/:postid/comments` (base URL `https://api.sleekplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-comments.md) for the provider-specific parameters and requirements.

