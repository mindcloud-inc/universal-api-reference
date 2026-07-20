# lobst.rs: Get Story by Slug

Retrieves a story from lobst.rs by slug.

```
GET https://connect.mindcloud.co/v1/universal/lobstrs/latest/actions/get-story-by-slug
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lobst.rs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lobstrs/latest/actions/get-story-by-slug?connectionId=$CONNECTION_ID&shortId=hedf1w&titleSlug=rust_should_have_stable_tail_calls" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shortId": "hedf1w",
  "titleSlug": "rust_should_have_stable_tail_calls"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lobstrs/latest/actions/get-story-by-slug?${params}`, {
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
| `shortId` | string | yes | Lobsters story short ID, such as hedf1w. Example: `hedf1w`. |
| `titleSlug` | string | yes | Story title slug from the canonical Lobsters URL. Example: `rust_should_have_stable_tail_calls`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment_count": 1,
      "comments": [
        {}
      ],
      "comments_url": "https://example.com",
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "description_plain": "string",
      "flags": 1,
      "score": 1,
      "short_id": "string",
      "short_id_url": "https://example.com",
      "submitter_user": "string",
      "tags": [
        "string"
      ],
      "title": "string",
      "url": "https://example.com",
      "user_is_author": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment_count` | number |  |
| `comments` | array<object> |  |
| `comments_url` | string |  |
| `created_at` | date |  |
| `description` | string |  |
| `description_plain` | string |  |
| `flags` | number |  |
| `score` | number |  |
| `short_id` | string |  |
| `short_id_url` | string |  |
| `submitter_user` | string |  |
| `tags` | array<string> |  |
| `title` | string |  |
| `url` | string |  |
| `user_is_author` | boolean |  |

## Native endpoint

Through the native lobst.rs API, this operation is `GET /s/:shortId/:titleSlug.json` (base URL `https://lobste.rs`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-story-by-slug.md) for the provider-specific parameters and requirements.

