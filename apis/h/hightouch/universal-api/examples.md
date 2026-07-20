# Hightouch Universal API Examples

These examples use the MindCloud API key and Hightouch connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Destinations

Retrieves destinations from Hightouch.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/list-destinations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/list-destinations?${params}`, {
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
      "hasMore": true
    }
  ],
  "meta": {}
}
```

See the full [List Destinations action reference](actions/list-destinations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hightouch/latest/actions/list-destinations).

## Create Decision Engine Message

Creates a decision engine message in Hightouch.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/create-decision-engine-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "flowId": "string",
  "name": "Ava Chen",
  "channelId": "string",
  "config": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/create-decision-engine-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "flowId": "string",
    "name": "Ava Chen",
    "channelId": "string",
    "config": {}
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
      "channelId": "string",
      "config": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "guardrails": {},
      "id": "string",
      "name": "Ava Chen",
      "tags": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "variables": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Decision Engine Message action reference](actions/create-decision-engine-message.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hightouch/latest/actions/create-decision-engine-message).
