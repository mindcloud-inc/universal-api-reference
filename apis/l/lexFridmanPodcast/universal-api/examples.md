# Lex Fridman Podcast Universal API Examples

These examples use the MindCloud API key and Lex Fridman Podcast connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Category

Retrieves a category from Lex Fridman Podcast.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lexFridmanPodcast/latest/actions/get-category?connectionId=$CONNECTION_ID&id=3392" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "3392"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lexFridmanPodcast/latest/actions/get-category?${params}`, {
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
      "count": 1,
      "description": "string",
      "id": 1,
      "link": "https://example.com",
      "name": "Ava Chen",
      "parent": 1,
      "slug": "string",
      "taxonomy": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Category action reference](actions/get-category.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lexFridmanPodcast/latest/actions/get-category).
