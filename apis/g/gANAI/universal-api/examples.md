# GAN.AI Universal API Examples

These examples use the MindCloud API key and GAN.AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Voices

Retrieves available voice profiles from GAN.AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/list-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/list-voices?${params}`, {
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
      "voiceDescription": "string",
      "voiceId": "string",
      "voiceName": "Ava Chen",
      "voiceSample": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Voices action reference](actions/list-voices.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gANAI/latest/actions/list-voices).

## Add Voice

Creates a custom voice in GAN.AI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/add-voice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/add-voice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
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
      "voiceDescription": "string",
      "voiceId": "string",
      "voiceName": "Ava Chen",
      "voiceSample": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Voice action reference](actions/add-voice.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gANAI/latest/actions/add-voice).
