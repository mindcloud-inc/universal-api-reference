# LiveChat: List Archives

Retrieves archived chats and thread events from LiveChat.

```
GET https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/list-archives
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LiveChat `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/list-archives?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/list-archives?${params}`, {
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
| `filters` | object | no | Archive search filters. |
| `filters.query` | string | no | Free-text archive query. |
| `filters.from` | date | no | Lower RFC3339 timestamp bound for archives. |
| `filters.to` | date | no | Upper RFC3339 timestamp bound for archives. |
| `filters.chatIds[]` | array<string> | no | Filter by chat IDs. |
| `filters.threadIds[]` | array<string> | no | Filter by thread IDs. |
| `filters.groupIds[]` | array<number> | no | Filter by group IDs. |
| `filters.customerId` | string | no | Filter by customer ID. |
| `filters.customerEmail` | string | no | Filter by customer email. |
| `sortOrder` | string | no | Default desc. Default: `desc`. |

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
        "nextAccessibleThreadId": "string",
        "nextThreadId": "string",
        "previousAccessibleThreadId": "string",
        "previousThreadId": "string",
        "properties": {},
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
          "avatar": "string",
          "email": "ava@example.com",
          "id": "string",
          "name": "Ava Chen",
          "present": true,
          "type": "string",
          "visibility": "string"
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
| `thread` | object | Archived thread details. |
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
| `thread.events` | array<object> | Events in the archived thread. |
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
| `thread.nextAccessibleThreadId` | string | Identifier of the next accessible thread. |
| `thread.nextThreadId` | string | Identifier of the next thread. |
| `thread.previousAccessibleThreadId` | string | Identifier of the previous accessible thread. |
| `thread.previousThreadId` | string | Identifier of the previous thread. |
| `thread.properties` | object | Properties assigned to the thread. |
| `thread.summary` | object | AI-generated summary of the thread, when available. |
| `thread.summary.status` | string | Status of the summary generation. |
| `thread.summary.text` | string | Summary text. |
| `thread.summary.updatedAt` | date | Time when the summary was updated. |
| `thread.tags` | array<string> | Tags assigned to the thread. |
| `thread.userIds` | array<string> | Identifiers of users in the thread. |
| `users` | array<object> | Users participating in the archived chat. |
| `users[].avatar` | string | Avatar URL for the user. |
| `users[].email` | string | User email address, when available. |
| `users[].id` | string | User identifier. |
| `users[].name` | string | User name. |
| `users[].present` | boolean | Whether the user is currently present in the chat. |
| `users[].type` | string | User type. |
| `users[].visibility` | string | Visibility of the user in the chat. |

## Native endpoint

Through the native LiveChat API, this operation is `POST /list_archives` (base URL `https://api.livechatinc.com/v3.6/agent/action`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-archives.md) for the provider-specific parameters and requirements.

