# Mighty Networks: List Post Comments

Retrieves comments for a Mighty Networks post.

```
GET https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/list-post-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mighty Networks `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/list-post-comments?connectionId=$CONNECTION_ID&limit=25&offset=0&networkId=%7B%7Bcredentials.networkId%7D%7D&postId=123456789" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "networkId": "{{credentials.networkId}}",
  "postId": "123456789"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/list-post-comments?${params}`, {
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
| `networkId` | string | yes | The Mighty Networks network ID or subdomain for the request path. Default: `{{credentials.networkId}}`. |
| `postId` | number | yes | The ID of the post whose comments you want to list. Example: `123456789`. |

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

Through the native Mighty Networks API, this operation is `GET /networks/:network_id/posts/:post_id/comments` (base URL `https://api.mn.co/admin/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-post-comments.md) for the provider-specific parameters and requirements.

