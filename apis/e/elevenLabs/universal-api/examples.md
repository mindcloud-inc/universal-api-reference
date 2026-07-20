# ElevenLabs Universal API Examples

These examples use the MindCloud API key and ElevenLabs connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Models

Retrieves a list of models from ElevenLabs.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/elevenLabs/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/elevenLabs/latest/actions/list-models?${params}`, {
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

See the full [List Models action reference](actions/list-models.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/elevenLabs/latest/actions/list-models).

## Convert Speech To Speech

Transforms audio from one voice to another in ElevenLabs.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/elevenLabs/latest/actions/convert-speech-to-speech" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "voiceId": "string",
  "audio": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/elevenLabs/latest/actions/convert-speech-to-speech', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "voiceId": "string",
    "audio": "string"
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

See the full [Convert Speech To Speech action reference](actions/convert-speech-to-speech.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/elevenLabs/latest/actions/convert-speech-to-speech).
