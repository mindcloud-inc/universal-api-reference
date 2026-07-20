# Creator Science Podcast Universal API Examples

These examples use the MindCloud API key and Creator Science Podcast connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Podcast Episodes

Retrieves podcast episodes from the Creator Science Podcast feed.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/creatorSciencePodcast/latest/actions/list-podcast-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/creatorSciencePodcast/latest/actions/list-podcast-episodes?${params}`, {
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
      "audioType": "string",
      "audioUrl": "https://example.com",
      "author": "Ava Chen",
      "contentHtml": "string",
      "description": "string",
      "durationSeconds": 1,
      "episodeNumber": 1,
      "episodeType": "string",
      "guid": "string",
      "id": "string",
      "imageUrl": "https://example.com",
      "isExplicit": true,
      "link": "https://example.com",
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "rawTitle": "string",
      "seasonNumber": 1,
      "subtitle": "string",
      "summary": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Podcast Episodes action reference](actions/list-podcast-episodes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/creatorSciencePodcast/latest/actions/list-podcast-episodes).
