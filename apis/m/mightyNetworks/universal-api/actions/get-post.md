# Mighty Networks: Get Post

Retrieves a post from Mighty Networks.

```
GET https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/get-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mighty Networks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/get-post?connectionId=$CONNECTION_ID&networkId=%7B%7Bcredentials.networkId%7D%7D&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "networkId": "{{credentials.networkId}}",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/get-post?${params}`, {
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
| `networkId` | string | yes | Network ID. Default: `{{credentials.networkId}}`. |
| `id` | number | yes | Post ID. |

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

Through the native Mighty Networks API, this operation is `GET /networks/:network_id/posts/:id/` (base URL `https://api.mn.co/admin/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-post.md) for the provider-specific parameters and requirements.

