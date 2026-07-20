# Birdie Screen Recording Universal API Examples

These examples use the MindCloud API key and Birdie Screen Recording connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Recordings

Retrieves recordings from Birdie Screen Recording.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/birdieScreenRecording/latest/actions/list-recordings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/birdieScreenRecording/latest/actions/list-recordings?${params}`, {
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

See the full [List Recordings action reference](actions/list-recordings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/birdieScreenRecording/latest/actions/list-recordings).
