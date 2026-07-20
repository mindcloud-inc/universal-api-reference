# LiveChat: Get Customer

Retrieves detailed customer information from LiveChat.

```
GET https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LiveChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/get-customer?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/get-customer?${params}`, {
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
| `id` | string | yes | The customer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentLastEventCreatedAt": "2026-05-07T12:00:00.000Z",
      "avatar": "string",
      "chatIds": [
        "string"
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customerLastEventCreatedAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "emailVerified": true,
      "eventsSeenUpTo": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "omnichannel": {},
      "phoneNumber": "string",
      "present": true,
      "sessionFields": [
        {}
      ],
      "state": "string",
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
        "referrer": "string",
        "startedAt": "2026-05-07T12:00:00.000Z",
        "userAgent": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentLastEventCreatedAt` | date | Timestamp of the latest agent event for the customer. |
| `avatar` | string | Avatar URL for the customer. |
| `chatIds` | array<string> | Identifiers of chats related to the customer. |
| `createdAt` | date | Time when the customer identity was created. |
| `customerLastEventCreatedAt` | date | Timestamp of the latest customer event for the customer. |
| `email` | string | Customer email address, when available. |
| `emailVerified` | boolean | Whether the customer's email is verified. |
| `eventsSeenUpTo` | date | Latest event timestamp seen by the customer. |
| `id` | string | Customer identifier. |
| `name` | string | Customer name, when available. |
| `omnichannel` | object | Omnichannel data for connected channels. |
| `phoneNumber` | string | Customer phone number. |
| `present` | boolean | Whether the customer is currently present. |
| `sessionFields` | array<object> | Custom session fields for the customer. |
| `state` | string | Current customer state. |
| `statistics` | object | Customer activity counters. |
| `statistics.chatsCount` | number | Number of chats for the customer. |
| `statistics.greetingsAcceptedCount` | number | Number of greetings accepted by the customer. |
| `statistics.greetingsShownCount` | number | Number of greetings shown to the customer. |
| `statistics.pageViewsCount` | number | Number of page views for the customer. |
| `statistics.threadsCount` | number | Number of threads for the customer. |
| `statistics.ticketsCount` | number | Number of tickets related to the customer. |
| `statistics.visitsCount` | number | Number of visits for the customer. |
| `tickets` | array<object> | Tickets related to the customer. |
| `tickets[].createdAt` | date | Time when the ticket was created. |
| `tickets[].ticketId` | string | Ticket identifier. |
| `type` | string | Resource type. |
| `visit` | object | Most recent online visit details. |
| `visit.endedAt` | date | Time when the visit ended. |
| `visit.geolocation` | object | Visit geolocation details. |
| `visit.geolocation.city` | string | Visitor city. |
| `visit.geolocation.country` | string | Visitor country. |
| `visit.geolocation.countryCode` | string | Visitor country code. |
| `visit.geolocation.latitude` | string | Visitor latitude. |
| `visit.geolocation.longitude` | string | Visitor longitude. |
| `visit.geolocation.region` | string | Visitor region. |
| `visit.geolocation.timezone` | string | Visitor timezone. |
| `visit.ip` | string | Visitor IP address. |
| `visit.lastPages` | array<object> | Most recent pages visited by the customer. |
| `visit.lastPages[].openedAt` | date | Time when the page was opened. |
| `visit.lastPages[].title` | string | Visited page title. |
| `visit.lastPages[].url` | string | Visited page URL. |
| `visit.referrer` | string | Visit referrer URL. |
| `visit.startedAt` | date | Time when the visit started. |
| `visit.userAgent` | string | Visitor user agent. |

## Native endpoint

Through the native LiveChat API, this operation is `POST /get_customer` (base URL `https://api.livechatinc.com/v3.6/agent/action`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

