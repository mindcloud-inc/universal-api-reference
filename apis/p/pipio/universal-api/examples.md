# Pipio Universal API Examples

These examples use the MindCloud API key and Pipio connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Languages

Finds supported voice languages in Pipio.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipio/latest/actions/list-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipio/latest/actions/list-languages?${params}`, {
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

See the full [List Languages action reference](actions/list-languages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pipio/latest/actions/list-languages).

## Generate Dubbed Video Legacy

Creates a dubbed video in Pipio using the legacy workflow.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pipio/latest/actions/generate-dubbed-video-legacy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetLanguage": "es",
  "sourceUrl": "https://cdn.pipio.ai/your-video.mp4"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipio/latest/actions/generate-dubbed-video-legacy', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetLanguage": "es",
    "sourceUrl": "https://cdn.pipio.ai/your-video.mp4"
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

See the full [Generate Dubbed Video Legacy action reference](actions/generate-dubbed-video-legacy.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pipio/latest/actions/generate-dubbed-video-legacy).
