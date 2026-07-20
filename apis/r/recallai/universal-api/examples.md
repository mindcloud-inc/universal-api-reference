# Recallai Universal API Examples

These examples use the MindCloud API key and Recallai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Bots

Retrieves bots from Recallai.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recallai/latest/actions/list-bots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recallai/latest/actions/list-bots?${params}`, {
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
      "automaticLeave": {},
      "botName": "Ava Chen",
      "calendarMeetings": [
        "string"
      ],
      "id": "string",
      "joinAt": "string",
      "meetingUrl": {},
      "metadata": {},
      "recordingConfig": {},
      "recordings": [
        "string"
      ],
      "statusChanges": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Bots action reference](actions/list-bots.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/recallai/latest/actions/list-bots).

## Create Bot

Creates a new bot in Recallai.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recallai/latest/actions/create-bot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "meetingUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recallai/latest/actions/create-bot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "meetingUrl": "https://example.com"
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
      "automaticLeave": {},
      "botName": "Ava Chen",
      "calendarMeetings": [
        "string"
      ],
      "id": "string",
      "joinAt": "string",
      "meetingUrl": {},
      "metadata": {},
      "recordingConfig": {},
      "recordings": [
        "string"
      ],
      "statusChanges": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Bot action reference](actions/create-bot.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/recallai/latest/actions/create-bot).
