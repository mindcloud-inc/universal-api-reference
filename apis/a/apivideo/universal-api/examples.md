# api.video Universal API Examples

These examples use the MindCloud API key and api.video connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List all video objects

Retrieves all video objects from api.video.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apivideo/latest/actions/list-videos?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apivideo/latest/actions/list-videos?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List all video objects action reference](actions/list-videos.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/apivideo/latest/actions/list-videos).

## Complete a live stream

Requests completion of a live stream in api.video.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/apivideo/latest/actions/complete-a-live-stream" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "liveStreamId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apivideo/latest/actions/complete-a-live-stream', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "liveStreamId": "string"
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

See the full [Complete a live stream action reference](actions/complete-a-live-stream.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/apivideo/latest/actions/complete-a-live-stream).
