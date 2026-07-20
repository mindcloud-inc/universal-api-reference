# Murf Core Universal API Examples

These examples use the MindCloud API key and Murf Core connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Voices

Retrieves available voices from Murf Core.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/murfCore/latest/actions/list-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/murfCore/latest/actions/list-voices?${params}`, {
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
      "accent": "string",
      "availableStyles": [
        "string"
      ],
      "description": "string",
      "displayLanguage": "string",
      "displayName": "Ava Chen",
      "gender": "string",
      "locale": "string",
      "supportedLocales": {},
      "voiceId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Voices action reference](actions/list-voices.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/murfCore/latest/actions/list-voices).

## Synthesize Speech

Synthesizes speech from text in Murf Core.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/murfCore/latest/actions/synthesize-speech" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "text": "string",
  "voiceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/murfCore/latest/actions/synthesize-speech', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "text": "string",
    "voiceId": "string"
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
      "audioFile": "string",
      "audioLengthInSeconds": 1,
      "consumedCharacterCount": 1,
      "encodedAudio": "string",
      "remainingCharacterCount": 1,
      "warning": "string",
      "wordDurations": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Synthesize Speech action reference](actions/synthesize-speech.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/murfCore/latest/actions/synthesize-speech).
