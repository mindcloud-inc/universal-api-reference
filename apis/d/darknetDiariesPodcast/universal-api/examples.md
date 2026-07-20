# Darknet Diaries Podcast Universal API Examples

These examples use the MindCloud API key and Darknet Diaries Podcast connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Episode By GUID

Retrieves a podcast episode by GUID from Darknet Diaries Podcast.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/darknetDiariesPodcast/latest/actions/get-episode-by-guid?connectionId=$CONNECTION_ID&guid=prx_7057_cb64ead7-d1f0-41c4-885c-84ce8b3e42d9" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guid": "prx_7057_cb64ead7-d1f0-41c4-885c-84ce8b3e42d9"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/darknetDiariesPodcast/latest/actions/get-episode-by-guid?${params}`, {
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
      "seasonNumber": 1,
      "summary": "string",
      "title": "string",
      "transcriptType": "string",
      "transcriptUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Episode By GUID action reference](actions/get-episode-by-guid.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/darknetDiariesPodcast/latest/actions/get-episode-by-guid).
