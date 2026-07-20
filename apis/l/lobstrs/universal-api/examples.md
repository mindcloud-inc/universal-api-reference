# lobst.rs Universal API Examples

These examples use the MindCloud API key and lobst.rs connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Find Stories by URL

Finds stories in lobst.rs by URL.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lobstrs/latest/actions/find-stories-by-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fgithub.com%2Fjemalloc%2Fjemalloc%2Freleases%2Ftag%2F5.3.1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://github.com/jemalloc/jemalloc/releases/tag/5.3.1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lobstrs/latest/actions/find-stories-by-url?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

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

See the full [Find Stories by URL action reference](actions/find-stories-by-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lobstrs/latest/actions/find-stories-by-url).
