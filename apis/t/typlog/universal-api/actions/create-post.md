# Typlog: Create Post

Creates a new post in Typlog.

```
POST https://connect.mindcloud.co/v1/universal/typlog/latest/actions/create-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typlog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/typlog/latest/actions/create-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "siteId": "4863",
  "title": "My First Post",
  "slug": "my-first-post",
  "lang": "en",
  "format": "markdown"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typlog/latest/actions/create-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "siteId": "4863",
    "title": "My First Post",
    "slug": "my-first-post",
    "lang": "en",
    "format": "markdown"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `siteId` | number | yes | Typlog site ID used to set the X-Site-Id header. Example: `4863`. |
| `title` | string | yes | Post title. Example: `My First Post`. |
| `slug` | string | yes | Post slug. Example: `my-first-post`. |
| `lang` | string | yes | Post language code. Example: `en`. |
| `format` | string | yes | Post content format. Example: `markdown`. |
| `subtitle` | string | no | Post subtitle. |
| `visibility` | string | no | Post visibility. Example: `public`. |
| `comment` | string | no | Comment setting. Example: `open`. |
| `tags[]` | array<number> | no | Tag IDs. |
| `primaryAuthors[]` | array<number> | no | Primary author IDs. |
| `secondaryAuthors[]` | array<number> | no | Secondary author IDs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "comment": "string",
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "format": "string",
      "id": 1,
      "lang": "string",
      "license": "string",
      "metadata": {},
      "primaryAuthors": [
        {}
      ],
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "replyTo": "string",
      "secondaryAuthors": [
        {}
      ],
      "slug": "string",
      "status": "string",
      "subtitle": "string",
      "tags": [
        {}
      ],
      "title": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `comment` | string |  |
| `content` | string |  |
| `createdAt` | date |  |
| `format` | string |  |
| `id` | number |  |
| `lang` | string |  |
| `license` | string |  |
| `metadata` | object |  |
| `primaryAuthors` | array<object> |  |
| `publishedAt` | date |  |
| `replyTo` | string |  |
| `secondaryAuthors` | array<object> |  |
| `slug` | string |  |
| `status` | string |  |
| `subtitle` | string |  |
| `tags` | array<object> |  |
| `title` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Typlog API, this operation is `POST /posts` (base URL `https://api.typlog.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-post.md) for the provider-specific parameters and requirements.

