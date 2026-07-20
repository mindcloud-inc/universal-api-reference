# LiveChat: Get Chat

Retrieves a chat with thread details from LiveChat.

```
GET https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/get-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LiveChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/get-chat?connectionId=$CONNECTION_ID&chatId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/get-chat?${params}`, {
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
| `chatId` | string | yes | The ID of the chat to fetch. |
| `threadId` | string | no | The thread ID to fetch. Defaults to the latest thread if omitted. |

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
      "properties": {},
      "thread": {
        "access": {
          "groupIds": [
            1
          ]
        },
        "active": true,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "customerVisit": {
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
          "userAgent": "string"
        },
        "events": [
          {
            "authorId": "string",
            "createdAt": "2026-05-07T12:00:00.000Z",
            "customId": "string",
            "deleted": true,
            "id": "string",
            "properties": {},
            "text": "string",
            "type": "string",
            "visibility": "string"
          }
        ],
        "id": "string",
        "nextThreadId": "string",
        "previousThreadId": "string",
        "properties": {},
        "queue": {
          "position": 1,
          "queuedAt": "2026-05-07T12:00:00.000Z",
          "waitTime": 1
        },
        "restrictedAccess": "string",
        "summary": {
          "status": "string",
          "text": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        },
        "tags": [
          "string"
        ],
        "userIds": [
          "string"
        ]
      },
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
| `properties` | object | Properties assigned to the chat. |
| `thread` | object | Requested thread details. |
| `thread.access` | object | Access settings for the thread. |
| `thread.access.groupIds` | array<number> | Group IDs that can access the thread. |
| `thread.active` | boolean | Whether the thread is active. |
| `thread.createdAt` | date | Time when the thread was created. |
| `thread.customerVisit` | object | Customer visit details associated with the thread. |
| `thread.customerVisit.geolocation` | object | Visit geolocation details. |
| `thread.customerVisit.geolocation.city` | string | Visitor city. |
| `thread.customerVisit.geolocation.country` | string | Visitor country. |
| `thread.customerVisit.geolocation.countryCode` | string | Visitor country code. |
| `thread.customerVisit.geolocation.latitude` | string | Visitor latitude. |
| `thread.customerVisit.geolocation.longitude` | string | Visitor longitude. |
| `thread.customerVisit.geolocation.region` | string | Visitor region. |
| `thread.customerVisit.geolocation.timezone` | string | Visitor timezone. |
| `thread.customerVisit.ip` | string | Visitor IP address. |
| `thread.customerVisit.userAgent` | string | Visitor user agent. |
| `thread.events` | array<object> | Events in the thread. |
| `thread.events[].authorId` | string | Author identifier for the event. |
| `thread.events[].createdAt` | date | Time when the event was created. |
| `thread.events[].customId` | string | Custom event identifier, when provided. |
| `thread.events[].deleted` | boolean | Whether the event represents a deleted event. |
| `thread.events[].id` | string | Event identifier. |
| `thread.events[].properties` | object | Properties assigned to the event. |
| `thread.events[].text` | string | Event text. |
| `thread.events[].type` | string | Event type. |
| `thread.events[].visibility` | string | Event visibility. |
| `thread.id` | string | Thread identifier. |
| `thread.nextThreadId` | string | Identifier of the next thread. |
| `thread.previousThreadId` | string | Identifier of the previous thread. |
| `thread.properties` | object | Properties assigned to the thread. |
| `thread.queue` | object | Queue details for the thread, when queued. |
| `thread.queue.position` | number | Current queue position. |
| `thread.queue.queuedAt` | date | Time when the thread entered the queue. |
| `thread.queue.waitTime` | number | Approximate wait time in seconds. |
| `thread.restrictedAccess` | string | Reason why thread access is restricted, when present. |
| `thread.summary` | object | AI-generated summary of the thread, when available. |
| `thread.summary.status` | string | Status of the summary generation. |
| `thread.summary.text` | string | Summary text. |
| `thread.summary.updatedAt` | date | Time when the summary was updated. |
| `thread.tags` | array<string> | Tags assigned to the thread. |
| `thread.userIds` | array<string> | Identifiers of users in the thread. |
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

Through the native LiveChat API, this operation is `POST /get_chat` (base URL `https://api.livechatinc.com/v3.6/agent/action`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chat.md) for the provider-specific parameters and requirements.

