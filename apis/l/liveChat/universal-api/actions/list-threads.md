# LiveChat: List Threads

Retrieves accessible chat threads from LiveChat.

```
GET https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/list-threads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LiveChat `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/list-threads?connectionId=$CONNECTION_ID&limit=25&offset=0&chatId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "chatId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/list-threads?${params}`, {
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
| `chatId` | string | yes | The ID of the chat. |
| `sortOrder` | string | no | Return oldest threads first with asc or newest threads first with desc. Default desc. Default: `desc`. |
| `minEventsCount` | number | no | Minimum total number of events to return across the latest threads. |
| `filters` | object | no | Date range filters for the listed threads. |
| `filters.from` | date | no | Lower RFC3339 timestamp bound for returned threads. |
| `filters.to` | date | no | Upper RFC3339 timestamp bound for returned threads. |

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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access` | object | Access settings for the thread. |
| `access.groupIds` | array<number> | Group IDs that can access the thread. |
| `active` | boolean | Whether the thread is active. |
| `createdAt` | date | Time when the thread was created. |
| `customerVisit` | object | Customer visit details associated with the thread. |
| `customerVisit.geolocation` | object | Visit geolocation details. |
| `customerVisit.geolocation.city` | string | Visitor city. |
| `customerVisit.geolocation.country` | string | Visitor country. |
| `customerVisit.geolocation.countryCode` | string | Visitor country code. |
| `customerVisit.geolocation.latitude` | string | Visitor latitude. |
| `customerVisit.geolocation.longitude` | string | Visitor longitude. |
| `customerVisit.geolocation.region` | string | Visitor region. |
| `customerVisit.geolocation.timezone` | string | Visitor timezone. |
| `customerVisit.ip` | string | Visitor IP address. |
| `customerVisit.userAgent` | string | Visitor user agent. |
| `events` | array<object> | Events in the thread. |
| `events[].authorId` | string | Author identifier for the event. |
| `events[].createdAt` | date | Time when the event was created. |
| `events[].customId` | string | Custom event identifier, when provided. |
| `events[].deleted` | boolean | Whether the event represents a deleted event. |
| `events[].id` | string | Event identifier. |
| `events[].properties` | object | Properties assigned to the event. |
| `events[].text` | string | Event text. |
| `events[].type` | string | Event type. |
| `events[].visibility` | string | Event visibility. |
| `id` | string | Thread identifier. |
| `nextThreadId` | string | Identifier of the next thread. |
| `previousThreadId` | string | Identifier of the previous thread. |
| `properties` | object | Properties assigned to the thread. |
| `queue` | object | Queue details for the thread, when queued. |
| `queue.position` | number | Current queue position. |
| `queue.queuedAt` | date | Time when the thread entered the queue. |
| `queue.waitTime` | number | Approximate wait time in seconds. |
| `restrictedAccess` | string | Reason why thread access is restricted, when present. |
| `summary` | object | AI-generated summary of the thread, when available. |
| `summary.status` | string | Status of the summary generation. |
| `summary.text` | string | Summary text. |
| `summary.updatedAt` | date | Time when the summary was updated. |
| `tags` | array<string> | Tags assigned to the thread. |
| `userIds` | array<string> | Identifiers of users in the thread. |

## Native endpoint

Through the native LiveChat API, this operation is `POST /list_threads` (base URL `https://api.livechatinc.com/v3.6/agent/action`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-threads.md) for the provider-specific parameters and requirements.

