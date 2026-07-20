# TED Radio Hour Podcast Universal API Examples

These examples use the MindCloud API key and TED Radio Hour Podcast connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Episodes

Retrieves episodes from the TED Radio Hour Podcast.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tEDRadioHourPodcast/latest/actions/list-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tEDRadioHourPodcast/latest/actions/list-episodes?${params}`, {
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
      "audioLength": 1,
      "audioType": "string",
      "audioUrl": "https://example.com",
      "contentEncoded": "string",
      "description": "string",
      "duration": 1,
      "episodeType": "string",
      "explicit": "string",
      "guid": "string",
      "imageUrl": "https://example.com",
      "link": "https://example.com",
      "pubDate": "2026-05-07T12:00:00.000Z",
      "thumbnailUrl": "https://example.com",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Episodes action reference](actions/list-episodes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tEDRadioHourPodcast/latest/actions/list-episodes).
