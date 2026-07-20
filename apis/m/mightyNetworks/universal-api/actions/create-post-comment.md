# Mighty Networks: Create Post Comment

Creates a comment on a post in Mighty Networks.

```
POST https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/create-post-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mighty Networks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/create-post-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "networkId": "{{credentials.networkId}}",
  "postId": "123456789",
  "text": "Thanks for sharing this."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/create-post-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "networkId": "{{credentials.networkId}}",
    "postId": "123456789",
    "text": "Thanks for sharing this."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `networkId` | string | yes | The Mighty Networks network ID or subdomain for the request path. Default: `{{credentials.networkId}}`. |
| `postId` | number | yes | The ID of the post where the comment will be created. Example: `123456789`. |
| `text` | string | yes | The content of the comment. Example: `Thanks for sharing this.`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `replyToId` | number | no | The ID of the parent comment when creating a reply. Example: `123456789`. |

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

Through the native Mighty Networks API, this operation is `POST /networks/:network_id/posts/:post_id/comments` (base URL `https://api.mn.co/admin/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-post-comment.md) for the provider-specific parameters and requirements.

