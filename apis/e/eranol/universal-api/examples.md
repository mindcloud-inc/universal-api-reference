# Eranol Universal API Examples

These examples use the MindCloud API key and Eranol connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify API Key

Verifies whether your Eranol API key is valid.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eranol/latest/actions/verify-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eranol/latest/actions/verify-api-key?${params}`, {
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

See the full [Verify API Key action reference](actions/verify-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eranol/latest/actions/verify-api-key).

## Add Background Audio

Creates a background audio job in Eranol.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eranol/latest/actions/add-background-audio" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "video_url": "https://example.com",
  "bg_audio_url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eranol/latest/actions/add-background-audio', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "video_url": "https://example.com",
    "bg_audio_url": "https://example.com"
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
      "jobId": "string",
      "jobType": "string",
      "message": "string",
      "resultUrl": "https://example.com",
      "status": "string",
      "statusUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Add Background Audio action reference](actions/add-background-audio.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eranol/latest/actions/add-background-audio).
