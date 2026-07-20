# Gladia Universal API Examples

These examples use the MindCloud API key and Gladia connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Pre-recorded Transcriptions

Retrieves pre-recorded transcription jobs from Gladia.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gladia/latest/actions/list-pre-recorded-transcriptions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gladia/latest/actions/list-pre-recorded-transcriptions?${params}`, {
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
      "current": "string",
      "first": "string",
      "items": [
        {}
      ],
      "next": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Pre-recorded Transcriptions action reference](actions/list-pre-recorded-transcriptions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gladia/latest/actions/list-pre-recorded-transcriptions).

## Create Legacy Audio Transcription

Creates a legacy audio transcription job in Gladia.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gladia/latest/actions/create-legacy-audio-transcription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "audioUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gladia/latest/actions/create-legacy-audio-transcription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "audioUrl": "https://example.com"
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
      "prediction": [
        {}
      ],
      "predictionRaw": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Legacy Audio Transcription action reference](actions/create-legacy-audio-transcription.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gladia/latest/actions/create-legacy-audio-transcription).
