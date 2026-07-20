# Mighty Networks: Get Post Comment

Retrieves a comment from a Mighty Networks post.

```
GET https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/get-post-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mighty Networks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/get-post-comment?connectionId=$CONNECTION_ID&networkId=%7B%7Bcredentials.networkId%7D%7D&postId=1&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "networkId": "{{credentials.networkId}}",
  "postId": "1",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/get-post-comment?${params}`, {
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
| `networkId` | string | yes | Default: `{{credentials.networkId}}`. |
| `postId` | number | yes |  |
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorId": 1,
      "cheerCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "depth": 1,
      "id": 1,
      "permalink": "https://example.com",
      "replyable": true,
      "replyCount": 1,
      "replyToId": 1,
      "spaceId": 1,
      "targetableId": 1,
      "targetableType": "string",
      "text": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorId` | number |  |
| `cheerCount` | number |  |
| `createdAt` | date |  |
| `depth` | number |  |
| `id` | number |  |
| `permalink` | string |  |
| `replyable` | boolean |  |
| `replyCount` | number |  |
| `replyToId` | number |  |
| `spaceId` | number |  |
| `targetableId` | number |  |
| `targetableType` | string |  |
| `text` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Mighty Networks API, this operation is `GET /networks/:network_id/posts/:post_id/comments/:id` (base URL `https://api.mn.co/admin/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-post-comment.md) for the provider-specific parameters and requirements.

