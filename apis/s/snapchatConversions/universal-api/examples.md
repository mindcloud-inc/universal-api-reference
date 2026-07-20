# Snapchat Conversions Universal API Examples

These examples use the MindCloud API key and Snapchat Conversions connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get App Signal Readiness Scores

Retrieves app signal readiness scores in Snapchat Conversions.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapchatConversions/latest/actions/get-app-signal-readiness-scores?connectionId=$CONNECTION_ID&snapAppId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "snapAppId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapchatConversions/latest/actions/get-app-signal-readiness-scores?${params}`, {
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

See the full [Get App Signal Readiness Scores action reference](actions/get-app-signal-readiness-scores.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/snapchatConversions/latest/actions/get-app-signal-readiness-scores).

## Send Achievement Unlocked Event

Creates an achievement unlocked conversion event in Snapchat Conversions.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/snapchatConversions/latest/actions/send-achievement-unlocked-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/snapchatConversions/latest/actions/send-achievement-unlocked-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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

See the full [Send Achievement Unlocked Event action reference](actions/send-achievement-unlocked-event.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/snapchatConversions/latest/actions/send-achievement-unlocked-event).
