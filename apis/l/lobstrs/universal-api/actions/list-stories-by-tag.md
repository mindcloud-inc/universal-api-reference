# lobst.rs: List Stories by Tag

Finds stories in lobst.rs by tag.

```
GET https://connect.mindcloud.co/v1/universal/lobstrs/latest/actions/list-stories-by-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lobst.rs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lobstrs/latest/actions/list-stories-by-tag?connectionId=$CONNECTION_ID&tag=rust" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tag": "rust"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lobstrs/latest/actions/list-stories-by-tag?${params}`, {
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
| `tag` | string | yes | Lobsters tag, or comma-separated tags such as rust,programming. Example: `rust`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment_count": 1,
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

Through the native lobst.rs API, this operation is `GET /t/:tag.json` (base URL `https://lobste.rs`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stories-by-tag.md) for the provider-specific parameters and requirements.

