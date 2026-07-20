# Simplecast Universal API Examples

These examples use the MindCloud API key and Simplecast connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Podcasts

Retrieves podcasts from Simplecast.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/list-podcasts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/list-podcasts?${params}`, {
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
      "collection": [
        {}
      ],
      "count": 1,
      "data": {},
      "description": "string",
      "href": "string",
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "title": "string",
      "total": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Podcasts action reference](actions/list-podcasts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/simplecast/latest/actions/list-podcasts).

## Upload Episode Audio

Uploads episode audio to Simplecast.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/upload-episode-audio" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "audioUrl": "https://example.com",
  "episodeId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/upload-episode-audio', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "audioUrl": "https://example.com",
    "episodeId": "string"
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
      "contentType": "string",
      "fileName": "Ava Chen",
      "href": "string",
      "id": "string",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Upload Episode Audio action reference](actions/upload-episode-audio.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/simplecast/latest/actions/upload-episode-audio).
