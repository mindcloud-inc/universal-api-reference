# Mighty Networks: Create Post

Creates a new post in Mighty Networks with optional notifications.

```
POST https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/create-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mighty Networks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/create-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "networkId": "{{credentials.networkId}}",
  "spaceId": 1,
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/create-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "networkId": "{{credentials.networkId}}",
    "spaceId": 1,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `networkId` | string | yes | Network ID. Default: `{{credentials.networkId}}`. |
| `spaceId` | number | yes | Space that will contain the new post. |
| `title` | string | yes | Post title. |
| `description` | string | no | Plain-text post content. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `postType` | string | no | Type of post to create, for example article. |
| `notify` | boolean | no | Notify the network about the new post. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commentsEnabled": true,
      "contentType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creatorId": 1,
      "description": "string",
      "id": 1,
      "lastActivityAt": "2026-05-07T12:00:00.000Z",
      "permalink": "https://example.com",
      "postType": "string",
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "spaceId": 1,
      "status": "string",
      "summary": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commentsEnabled` | boolean |  |
| `contentType` | string |  |
| `createdAt` | date |  |
| `creatorId` | number |  |
| `description` | string |  |
| `id` | number |  |
| `lastActivityAt` | date |  |
| `permalink` | string |  |
| `postType` | string |  |
| `publishedAt` | date |  |
| `spaceId` | number |  |
| `status` | string |  |
| `summary` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Mighty Networks API, this operation is `POST /networks/:network_id/posts` (base URL `https://api.mn.co/admin/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-post.md) for the provider-specific parameters and requirements.

