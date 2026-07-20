# Famulor AI - Voice Agent Universal API Examples

These examples use the MindCloud API key and Famulor AI - Voice Agent connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Call

Retrieves call details from Famulor.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/get-call?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/get-call?${params}`, {
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
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Call action reference](actions/get-call.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/famulorAIVoiceAgent/latest/actions/get-call).

## Create Assistant

Creates a new AI assistant in Famulor.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/create-assistant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "language_id": 1,
  "name": "Ava Chen",
  "voice_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/create-assistant', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "language_id": 1,
    "name": "Ava Chen",
    "voice_id": 1
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
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Assistant action reference](actions/create-assistant.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/famulorAIVoiceAgent/latest/actions/create-assistant).
