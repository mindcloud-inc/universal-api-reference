# Soniox Universal API Examples

These examples use the MindCloud API key and Soniox connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get models

Retrieves available transcription models from Soniox.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/soniox/latest/actions/get-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/soniox/latest/actions/get-models?${params}`, {
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
      "models": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get models action reference](actions/get-models.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/soniox/latest/actions/get-models).

## Create transcription

Creates a new transcription in Soniox.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/soniox/latest/actions/create-transcription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/soniox/latest/actions/create-transcription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "string"
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
      "audioDurationMs": 1,
      "audioUrl": "https://example.com",
      "clientReferenceId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "enableAudioEventDetection": true,
      "enableLanguageIdentification": true,
      "enableSpeakerDiarization": true,
      "errorMessage": "string",
      "errorType": "string",
      "fileId": "string",
      "filename": "Ava Chen",
      "id": "string",
      "languageHints": [
        "string"
      ],
      "model": "string",
      "status": "string",
      "webhookAuthHeaderName": "Ava Chen",
      "webhookAuthHeaderValue": "string",
      "webhookStatusCode": 1,
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create transcription action reference](actions/create-transcription.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/soniox/latest/actions/create-transcription).
