# Meetstream AI Universal API Examples

These examples use the MindCloud API key and Meetstream AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Bots

Retrieves bots from Meetstream AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/meetstreamAI/latest/actions/list-bots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/meetstreamAI/latest/actions/list-bots?${params}`, {
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

See the full [List Bots action reference](actions/list-bots.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/meetstreamAI/latest/actions/list-bots).

## Create Bot

Creates a new bot in Meetstream AI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/meetstreamAI/latest/actions/create-bot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "meetingLink": "https://example.com",
  "botName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/meetstreamAI/latest/actions/create-bot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "meetingLink": "https://example.com",
    "botName": "Ava Chen"
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
      "botId": "string",
      "joinAt": "string",
      "meetingUrl": "https://example.com",
      "scheduleName": "Ava Chen",
      "status": "string",
      "transcriptId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Bot action reference](actions/create-bot.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/meetstreamAI/latest/actions/create-bot).
