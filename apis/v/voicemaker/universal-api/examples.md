# Voicemaker Universal API Examples

These examples use the MindCloud API key and Voicemaker connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List VoxFX Effects

Retrieves available VoxFX effects from Voicemaker.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/list-vox-fx-effects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/list-vox-fx-effects?${params}`, {
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
      "data": [
        {}
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [List VoxFX Effects action reference](actions/list-vox-fx-effects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/voicemaker/latest/actions/list-vox-fx-effects).

## Convert Speech to Speech

Creates converted speech from uploaded audio in Voicemaker.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/convert-speech-to-speech" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "voiceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/convert-speech-to-speech', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
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
      "path": "string",
      "remainChars": 1,
      "remainKeyChars": 1,
      "success": true,
      "usedChars": 1
    }
  ],
  "meta": {}
}
```

See the full [Convert Speech to Speech action reference](actions/convert-speech-to-speech.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/voicemaker/latest/actions/convert-speech-to-speech).
