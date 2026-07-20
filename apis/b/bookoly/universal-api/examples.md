# Bookoly Universal API Examples

These examples use the MindCloud API key and Bookoly connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate API Token

Validates the current Bookoly API token.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/validate-api-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/validate-api-token?${params}`, {
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Validate API Token action reference](actions/validate-api-token.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bookoly/latest/actions/validate-api-token).

## Add Audio To Video

Adds audio to a video in Bookoly.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/add-audio-to-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "video": {},
  "video.name": "Ava Chen",
  "video.url": "https://example.com",
  "video.mute": true,
  "audio": {},
  "audio.url": "https://example.com",
  "audio.trim": true,
  "audio.volume": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/add-audio-to-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "video": {},
    "video.name": "Ava Chen",
    "video.url": "https://example.com",
    "video.mute": true,
    "audio": {},
    "audio.url": "https://example.com",
    "audio.trim": true,
    "audio.volume": 1
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Add Audio To Video action reference](actions/add-audio-to-video.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bookoly/latest/actions/add-audio-to-video).
