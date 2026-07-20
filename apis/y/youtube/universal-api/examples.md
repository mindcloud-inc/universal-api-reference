# YouTube Universal API Examples

These examples use the MindCloud API key and YouTube connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Channels

Retrieves one or more channels from YouTube.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-channels?connectionId=$CONNECTION_ID&limit=25&offset=0&part=snippet%2CcontentDetails%2Cstatistics" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "part": "snippet,contentDetails,statistics"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-channels?${params}`, {
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
      "contentDetails": {
        "relatedPlaylists": {
          "uploads": "string"
        }
      },
      "etag": "string",
      "id": "string",
      "kind": "string",
      "snippet": {
        "customUrl": "https://example.com",
        "description": "string",
        "publishedAt": "2026-05-07T12:00:00.000Z",
        "title": "string"
      },
      "statistics": {
        "subscriberCount": "string",
        "videoCount": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [List Channels action reference](actions/list-channels.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/youtube/latest/actions/list-channels).

## Create Playlist

Creates a new playlist in YouTube.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/youtube/latest/actions/create-playlist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "part": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/youtube/latest/actions/create-playlist', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "part": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "contentDetails": {
        "itemCount": 1
      },
      "etag": "string",
      "id": "string",
      "kind": "string",
      "player": {
        "embedHtml": "string"
      },
      "snippet": {
        "channelTitle": "string",
        "description": "string",
        "title": "string"
      },
      "status": {
        "privacyStatus": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Playlist action reference](actions/create-playlist.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/youtube/latest/actions/create-playlist).
