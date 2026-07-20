# LiveChat: List Chats

Retrieves accessible chat summaries from LiveChat.

```
GET https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/list-chats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LiveChat `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

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

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filters` | object | no | Filter options remembered across paginated requests. |
| `filters.active` | boolean | no | Return active chats only when true, inactive chats only when false. |
| `filters.includeChatsWithoutThreads` | boolean | no | Include chats without any threads in the returned summary. Default true. |
| `filters.groupIds[]` | array<number> | no | Filter by group IDs. Maximum 200 values. |
| `sortOrder` | string | no | Return oldest chats first with asc or newest chats first with desc. Default desc. Default: `desc`. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access` | object | Access settings for the chat. |
| `access.groupIds` | array<number> | Group IDs that can access the chat. |
| `id` | string | Chat identifier. |
| `isFollowed` | boolean | Whether the chat is followed by the requester. |
| `lastEventPerType` | object | Latest event grouped by event type. |
| `lastEventPerType.message` | object | Latest message event. |
| `lastEventPerType.message.event` | object | Latest message event payload. |
| `lastEventPerType.message.event.authorId` | string | Author identifier for the event. |
| `lastEventPerType.message.event.createdAt` | date | Time when the event was created. |
| `lastEventPerType.message.event.customId` | string | Custom identifier for the event, when provided. |
| `lastEventPerType.message.event.id` | string | Event identifier. |
| `lastEventPerType.message.event.properties` | object | Properties assigned to the event. |
| `lastEventPerType.message.event.text` | string | Event text. |
| `lastEventPerType.message.event.type` | string | Event type. |
| `lastEventPerType.message.threadCreatedAt` | date | Time when the related thread was created. |
| `lastEventPerType.message.threadId` | string | Thread identifier for the latest message event. |
| `lastEventPerType.systemMessage` | object | Latest system message event. |
| `lastEventPerType.systemMessage.event` | object | Latest system message payload. |
| `lastEventPerType.systemMessage.event.createdAt` | date | Time when the event was created. |
| `lastEventPerType.systemMessage.event.id` | string | Event identifier. |
| `lastEventPerType.systemMessage.event.systemMessageType` | string | System message classification. |
| `lastEventPerType.systemMessage.event.text` | string | System message text. |
| `lastEventPerType.systemMessage.event.textVars` | object | Template variables used in the system message. |
| `lastEventPerType.systemMessage.event.type` | string | Event type. |
| `lastEventPerType.systemMessage.threadCreatedAt` | date | Time when the related thread was created. |
| `lastEventPerType.systemMessage.threadId` | string | Thread identifier for the latest system message. |
| `lastThreadSummary` | object | Summary of the latest thread in the chat. |
| `lastThreadSummary.access` | object | Access settings for the latest thread. |
| `lastThreadSummary.access.groupIds` | array<number> | Group IDs that can access the latest thread. |
| `lastThreadSummary.active` | boolean | Whether the latest thread is active. |
| `lastThreadSummary.createdAt` | date | Time when the latest thread was created. |
| `lastThreadSummary.id` | string | Latest thread identifier. |
| `lastThreadSummary.properties` | object | Properties assigned to the latest thread. |
| `lastThreadSummary.queue` | object | Queue details for the latest thread, when queued. |
| `lastThreadSummary.queue.position` | number | Current queue position. |
| `lastThreadSummary.queue.queuedAt` | date | Time when the chat entered the queue. |
| `lastThreadSummary.queue.waitTime` | number | Approximate wait time in seconds. |
| `lastThreadSummary.userIds` | array<string> | Identifiers of users in the latest thread. |
| `properties` | object | Properties assigned to the chat. |
| `users` | array<object> | Users participating in the chat. |
| `users[].agentLastEventCreatedAt` | date | Timestamp of the latest agent event for the user. |
| `users[].avatar` | string | Avatar URL for the user. |
| `users[].createdAt` | date | Time when the user identity was created. |
| `users[].customerLastEventCreatedAt` | date | Timestamp of the latest customer event for the user. |
| `users[].email` | string | User email address, when available. |
| `users[].eventsSeenUpTo` | date | Latest event timestamp seen by the user. |
| `users[].id` | string | User identifier. |
| `users[].name` | string | User name. |
| `users[].present` | boolean | Whether the user is currently present in the chat. |
| `users[].statistics` | object | Customer activity counters. |
| `users[].statistics.chatsCount` | number | Number of chats for the user. |
| `users[].statistics.greetingsAcceptedCount` | number | Number of greetings accepted by the user. |
| `users[].statistics.greetingsShownCount` | number | Number of greetings shown to the user. |
| `users[].statistics.pageViewsCount` | number | Number of page views for the user. |
| `users[].statistics.threadsCount` | number | Number of threads for the user. |
| `users[].statistics.ticketsCount` | number | Number of tickets related to the user. |
| `users[].statistics.visitsCount` | number | Number of visits for the user. |
| `users[].tickets` | array<object> | Tickets related to the user. |
| `users[].tickets[].createdAt` | date | Time when the ticket was created. |
| `users[].tickets[].ticketId` | string | Ticket identifier. |
| `users[].type` | string | User type. |
| `users[].visit` | object | Most recent visit details for a customer user. |
| `users[].visit.endedAt` | date | Time when the visit ended. |
| `users[].visit.geolocation` | object | Visit geolocation details. |
| `users[].visit.geolocation.city` | string | Visitor city. |
| `users[].visit.geolocation.country` | string | Visitor country. |
| `users[].visit.geolocation.countryCode` | string | Visitor country code. |
| `users[].visit.geolocation.latitude` | string | Visitor latitude. |
| `users[].visit.geolocation.longitude` | string | Visitor longitude. |
| `users[].visit.geolocation.region` | string | Visitor region. |
| `users[].visit.geolocation.timezone` | string | Visitor timezone. |
| `users[].visit.ip` | string | Visitor IP address. |
| `users[].visit.lastPages` | array<object> | Most recent pages visited by the user. |
| `users[].visit.lastPages[].openedAt` | date | Time when the page was opened. |
| `users[].visit.lastPages[].title` | string | Visited page title. |
| `users[].visit.lastPages[].url` | string | Visited page URL. |
| `users[].visit.startedAt` | date | Time when the visit started. |
| `users[].visit.userAgent` | string | Visitor user agent. |

## Native endpoint

Through the native LiveChat API, this operation is `POST /list_chats` (base URL `https://api.livechatinc.com/v3.6/agent/action`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-chats.md) for the provider-specific parameters and requirements.

