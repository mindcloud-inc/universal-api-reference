# Hy.page: Get Post



```
GET https://connect.mindcloud.co/v1/universal/hypage/latest/actions/get-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hy.page `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hypage/latest/actions/get-post?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hypage/latest/actions/get-post?${params}`, {
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
| `id` | string | yes | Post ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": {},
      "authorId": "string",
      "categoryIds": [
        "string"
      ],
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "image": "string",
      "mediaAttachments": [
        {}
      ],
      "postType": "string",
      "price": 1,
      "pricingType": "string",
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "slug": "string",
      "status": "string",
      "tags": [
        "string"
      ],
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
| `author` | object |  |
| `authorId` | string |  |
| `categoryIds` | array<string> |  |
| `content` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | string |  |
| `image` | string |  |
| `mediaAttachments` | array<object> |  |
| `postType` | string |  |
| `price` | number |  |
| `pricingType` | string |  |
| `publishedAt` | date |  |
| `slug` | string |  |
| `status` | string |  |
| `tags` | array<string> |  |
| `title` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Hy.page API, this operation is `GET /hyax-api/v1/posts/:id` (base URL `https://platform.hyax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-post.md) for the provider-specific parameters and requirements.

