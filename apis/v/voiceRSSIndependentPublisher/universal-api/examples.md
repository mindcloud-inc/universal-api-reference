# VoiceRSS (Independent Publisher) Universal API Examples

These examples use the MindCloud API key and VoiceRSS (Independent Publisher) connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Convert Text to Speech

Creates speech audio from text in VoiceRSS.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voiceRSSIndependentPublisher/latest/actions/convert-text-to-speech" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "language": "en-us",
  "source_text": "Hello, world!"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voiceRSSIndependentPublisher/latest/actions/convert-text-to-speech', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "language": "en-us",
    "source_text": "Hello, world!"
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
      "audioContent": "string",
      "contentLength": 1
    }
  ],
  "meta": {}
}
```

See the full [Convert Text to Speech action reference](actions/convert-text-to-speech.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/voiceRSSIndependentPublisher/latest/actions/convert-text-to-speech).
