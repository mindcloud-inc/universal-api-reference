# AskHandle Universal API Examples

These examples use the MindCloud API key and AskHandle connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Rooms

Retrieves room records from your AskHandle account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/askhandle/latest/actions/list-rooms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/askhandle/latest/actions/list-rooms?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "greetingMessage": "string",
      "isBotUse": true,
      "isConfirmedForm": true,
      "isSchedulingOnly": true,
      "label": "string",
      "messages": [
        [
          {}
        ]
      ],
      "name": "Ava Chen",
      "rating": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Rooms action reference](actions/list-rooms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/askhandle/latest/actions/list-rooms).

## Create Message

Creates a new message in an AskHandle room.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/askhandle/latest/actions/create-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/askhandle/latest/actions/create-message', {
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
  "data": [
    {
      "body": "string",
      "email": "ava@example.com",
      "isSupportSender": true,
      "nickname": "Ava Chen",
      "phoneNumber": "string",
      "sentAt": "2026-05-07T12:00:00.000Z",
      "supportAnswer": "string",
      "terminated": true,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Message action reference](actions/create-message.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/askhandle/latest/actions/create-message).
