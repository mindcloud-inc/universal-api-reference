# Hy.page: Update Post



```
PUT https://connect.mindcloud.co/v1/universal/hypage/latest/actions/update-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hy.page `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hypage/latest/actions/update-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hypage/latest/actions/update-post', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | no | Updated post content. |
| `id` | string | yes | Post ID. |
| `slug` | string | no | Updated post slug. |
| `status` | string | no | Updated post status. |
| `tags` | string | no | Updated post tags. |
| `title` | string | no | Updated post title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorId": "string",
      "id": "string",
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "slug": "string",
      "status": "string",
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
| `authorId` | string |  |
| `id` | string |  |
| `publishedAt` | date |  |
| `slug` | string |  |
| `status` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Hy.page API, this operation is `PATCH /hyax-api/v1/posts/:id` (base URL `https://platform.hyax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-post.md) for the provider-specific parameters and requirements.

