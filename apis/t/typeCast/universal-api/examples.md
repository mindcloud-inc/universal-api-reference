# TypeCast Universal API Examples

These examples use the MindCloud API key and TypeCast connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Subscription

Retrieves current subscription details from TypeCast.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typeCast/latest/actions/get-subscription?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typeCast/latest/actions/get-subscription?${params}`, {
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
      "credits": {
        "planCredits": 1,
        "usedCredits": 1
      },
      "limits": {
        "concurrencyLimit": 1
      },
      "plan": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Subscription action reference](actions/get-subscription.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/typeCast/latest/actions/get-subscription).

## Streaming Text To Speech

Creates streaming speech audio in TypeCast.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/typeCast/latest/actions/streaming-text-to-speech" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "voiceId": "string",
  "text": "string",
  "model": "ssfm-v21"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typeCast/latest/actions/streaming-text-to-speech', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "voiceId": "string",
    "text": "string",
    "model": "ssfm-v21"
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

See the full [Streaming Text To Speech action reference](actions/streaming-text-to-speech.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/typeCast/latest/actions/streaming-text-to-speech).
