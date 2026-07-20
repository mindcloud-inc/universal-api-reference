# Sleekplan: Get Comment



```
GET https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/get-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sleekplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/get-comment?connectionId=$CONNECTION_ID&commentId=string&postId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "commentId": "string",
  "postId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/get-comment?${params}`, {
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
| `commentId` | string | yes |  |
| `postId` | string | yes |  |

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

Through the native Sleekplan API, this operation is `GET /post/:postid/comment/:commentid` (base URL `https://api.sleekplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-comment.md) for the provider-specific parameters and requirements.

