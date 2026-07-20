# No Stupid Questions Podcast Universal API Examples

These examples use the MindCloud API key and No Stupid Questions Podcast connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Episodes

Retrieves podcast episodes from No Stupid Questions Podcast.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/noStupidQuestionsPodcast/latest/actions/list-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/noStupidQuestionsPodcast/latest/actions/list-episodes?${params}`, {
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
      "audioLengthBytes": 1,
      "audioType": "string",
      "audioUrl": "https://example.com",
      "author": "string",
      "contentHtml": "string",
      "descriptionHtml": "string",
      "duration": "string",
      "episodeNumber": 1,
      "episodeTitle": "string",
      "episodeType": "string",
      "explicit": true,
      "guid": "string",
      "imageUrl": "https://example.com",
      "link": "https://example.com",
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "summary": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Episodes action reference](actions/list-episodes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/noStupidQuestionsPodcast/latest/actions/list-episodes).
