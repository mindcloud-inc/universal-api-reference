# Quanta Science Podcast Universal API Examples

These examples use the MindCloud API key and Quanta Science Podcast connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Podcast Episodes



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quantaSciencePodcast/latest/actions/list-podcast-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quantaSciencePodcast/latest/actions/list-podcast-episodes?${params}`, {
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
      "articleUrl": "https://example.com",
      "audioLength": 1,
      "audioType": "string",
      "audioUrl": "https://example.com",
      "author": "string",
      "description": "string",
      "descriptionHtml": "string",
      "duration": "string",
      "episodeType": "string",
      "guid": "string",
      "imageUrl": "https://example.com",
      "link": "https://example.com",
      "pubDate": "2026-05-07T12:00:00.000Z",
      "season": 1,
      "source": "string",
      "subtitle": "string",
      "summary": "string",
      "summaryHtml": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Podcast Episodes action reference](actions/list-podcast-episodes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/quantaSciencePodcast/latest/actions/list-podcast-episodes).
