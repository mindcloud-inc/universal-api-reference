# Dreamstudio Universal API Examples

These examples use the MindCloud API key and Dreamstudio connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credit Balance

Retrieves account credit balance from Dreamstudio.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dreamstudio/latest/actions/get-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dreamstudio/latest/actions/get-credit-balance?${params}`, {
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
      "credits": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Credit Balance action reference](actions/get-credit-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dreamstudio/latest/actions/get-credit-balance).

## Audio to Audio

Creates audio from an audio sample in Dreamstudio.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dreamstudio/latest/actions/audio-to-audio" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "string",
  "audio": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dreamstudio/latest/actions/audio-to-audio', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prompt": "string",
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

See the full [Audio to Audio action reference](actions/audio-to-audio.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dreamstudio/latest/actions/audio-to-audio).
