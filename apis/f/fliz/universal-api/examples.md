# Fliz Universal API Examples

These examples use the MindCloud API key and Fliz connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get video

Retrieves a video from your Fliz account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fliz/latest/actions/get-video?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fliz/latest/actions/get-video?${params}`, {
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
      "category": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "error": {},
      "format": "string",
      "id": "string",
      "lang": "string",
      "music": {},
      "remotionConfiguration": {},
      "step": "string",
      "title": "string",
      "url": "https://example.com",
      "voiceId": "string",
      "watermark": {}
    }
  ],
  "meta": {}
}
```

See the full [Get video action reference](actions/get-video.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fliz/latest/actions/get-video).

## Create video

Creates a new video in Fliz.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fliz/latest/actions/create-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "description": "string",
  "format": "0",
  "lang": "en"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fliz/latest/actions/create-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "description": "string",
    "format": "0",
    "lang": "en"
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
      "cost": 1,
      "videoId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create video action reference](actions/create-video.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fliz/latest/actions/create-video).
