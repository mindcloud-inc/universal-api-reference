# AiVOOV Universal API Examples

These examples use the MindCloud API key and AiVOOV connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Voices

Retrieves available voice IDs from AiVOOV.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aiVOOV/latest/actions/list-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aiVOOV/latest/actions/list-voices?${params}`, {
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
      "gender": "string",
      "label": "string",
      "languageCode": "string",
      "languageName": "Ava Chen",
      "name": "Ava Chen",
      "value": "string",
      "voiceId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Voices action reference](actions/list-voices.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aiVOOV/latest/actions/list-voices).

## Create Audio

Creates audio from multiple voice and text inputs in AiVOOV.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aiVOOV/latest/actions/create-audio" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "voiceIds": "string",
  "texts[]": "Hello from MindCloud"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aiVOOV/latest/actions/create-audio', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "voiceIds": "string",
    "texts[]": "Hello from MindCloud"
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

See the full [Create Audio action reference](actions/create-audio.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aiVOOV/latest/actions/create-audio).
