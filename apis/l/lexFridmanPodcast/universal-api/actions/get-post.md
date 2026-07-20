# Lex Fridman Podcast: Get Post

Retrieves a post from Lex Fridman Podcast.

```
GET https://connect.mindcloud.co/v1/universal/lexFridmanPodcast/latest/actions/get-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lex Fridman Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lexFridmanPodcast/latest/actions/get-post?connectionId=$CONNECTION_ID&id=6441" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "6441"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lexFridmanPodcast/latest/actions/get-post?${params}`, {
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
| `id` | string | yes | The post ID. Default: `6441`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": 1,
      "categories": [
        1
      ],
      "content": {},
      "date": "2026-05-07T12:00:00.000Z",
      "dateGmt": "2026-05-07T12:00:00.000Z",
      "excerpt": {},
      "featuredMedia": 1,
      "id": 1,
      "link": "https://example.com",
      "modified": "2026-05-07T12:00:00.000Z",
      "modifiedGmt": "2026-05-07T12:00:00.000Z",
      "slug": "string",
      "status": "string",
      "tags": [
        1
      ],
      "title": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | number |  |
| `categories` | array<number> |  |
| `content` | object |  |
| `date` | date |  |
| `dateGmt` | date |  |
| `excerpt` | object |  |
| `featuredMedia` | number |  |
| `id` | number |  |
| `link` | string |  |
| `modified` | date |  |
| `modifiedGmt` | date |  |
| `slug` | string |  |
| `status` | string |  |
| `tags` | array<number> |  |
| `title` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Lex Fridman Podcast API, this operation is `GET /wp-json/wp/v2/posts/:id` (base URL `https://lexfridman.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-post.md) for the provider-specific parameters and requirements.

