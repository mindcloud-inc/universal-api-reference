# LiveChat Universal API Examples

These examples use the MindCloud API key and LiveChat connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Chats

Retrieves accessible chat summaries from LiveChat.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/list-chats?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/list-chats?${params}`, {
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
      "access": {
        "groupIds": [
          1
        ]
      },
      "id": "string",
      "isFollowed": true,
      "lastEventPerType": {
        "message": {
          "event": {
            "authorId": "string",
            "createdAt": "2026-05-07T12:00:00.000Z",
            "customId": "string",
            "id": "string",
            "properties": {},
            "text": "string",
            "type": "string"
          },
          "threadCreatedAt": "2026-05-07T12:00:00.000Z",
          "threadId": "string"
        },
        "systemMessage": {
          "event": {
            "createdAt": "2026-05-07T12:00:00.000Z",
            "id": "string",
            "systemMessageType": "string",
            "text": "string",
            "textVars": {},
            "type": "string"
          },
          "threadCreatedAt": "2026-05-07T12:00:00.000Z",
          "threadId": "string"
        }
      },
      "lastThreadSummary": {
        "access": {
          "groupIds": [
            1
          ]
        },
        "active": true,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "properties": {},
        "queue": {
          "position": 1,
          "queuedAt": "2026-05-07T12:00:00.000Z",
          "waitTime": 1
        },
        "userIds": [
          "string"
        ]
      },
      "properties": {},
      "users": [
        {
          "agentLastEventCreatedAt": "2026-05-07T12:00:00.000Z",
          "avatar": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "customerLastEventCreatedAt": "2026-05-07T12:00:00.000Z",
          "email": "ava@example.com",
          "eventsSeenUpTo": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "name": "Ava Chen",
          "present": true,
          "statistics": {
            "chatsCount": 1,
            "greetingsAcceptedCount": 1,
            "greetingsShownCount": 1,
            "pageViewsCount": 1,
            "threadsCount": 1,
            "ticketsCount": 1,
            "visitsCount": 1
          },
          "tickets": [
            {
              "createdAt": "2026-05-07T12:00:00.000Z",
              "ticketId": "string"
            }
          ],
          "type": "string",
          "visit": {
            "endedAt": "2026-05-07T12:00:00.000Z",
            "geolocation": {
              "city": "string",
              "country": "string",
              "countryCode": "string",
              "latitude": "string",
              "longitude": "string",
              "region": "string",
              "timezone": "string"
            },
            "ip": "string",
            "lastPages": [
              {
                "openedAt": "2026-05-07T12:00:00.000Z",
                "title": "string",
                "url": "https://example.com"
              }
            ],
            "startedAt": "2026-05-07T12:00:00.000Z",
            "userAgent": "string"
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Chats action reference](actions/list-chats.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/liveChat/latest/actions/list-chats).

## Add User To Chat

Updates a chat by adding a user in LiveChat.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/add-user-to-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatId": "string",
  "userId": "string",
  "userType": "string",
  "visibility": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/add-user-to-chat', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatId": "string",
    "userId": "string",
    "userType": "string",
    "visibility": "string"
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
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add User To Chat action reference](actions/add-user-to-chat.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/liveChat/latest/actions/add-user-to-chat).
