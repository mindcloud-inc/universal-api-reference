# Livestorm: List Event Sessions

Retrieves sessions for an event from Livestorm.

```
GET https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/list-event-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Livestorm `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/list-event-sessions?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/list-event-sessions?${params}`, {
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
| `id` | string | yes | Event ID |
| `filter[status]` | string | no | Filter Sessions by status : 'upcoming', 'live', 'on_demand', 'past', 'past_not_started', 'canceled', 'draft' |
| `filter[dateFrom]` | date | no | Filter Sessions which ‘estimated_started_at’ attribute starts from the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[dateTo]` | date | no | Filter Sessions which ‘estimated_started_at’ attribute ends with the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[createdSince]` | date | no | Filter Sessions which ‘created_at’ attribute starts from the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[createdUntil]` | date | no | Filter Sessions which ‘created_at’ attribute ends with the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[updatedSince]` | date | no | Filter Sessions which ‘updated_at’ attribute starts from the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[updatedUntil]` | date | no | Filter Sessions which ‘updated_at’ attribute ends with the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[includeBreakoutRooms]` | string | no | Filter Sessions depending upon if they are breakout room sessions or not |
| `include` | string | no | Include Related Data Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "attendeesCount": 1,
        "canceledAt": 1,
        "createdAt": 1,
        "duration": 1,
        "endedAt": 1,
        "estimatedStartedAt": 1,
        "eventTypeId": "string",
        "name": "Ava Chen",
        "registrantsCount": 1,
        "roomLink": "https://example.com",
        "startedAt": 1,
        "status": "string",
        "timezone": "string",
        "updatedAt": 1
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.attendeesCount` | number |  |
| `attributes.canceledAt` | number |  |
| `attributes.createdAt` | number |  |
| `attributes.duration` | number |  |
| `attributes.endedAt` | number |  |
| `attributes.estimatedStartedAt` | number |  |
| `attributes.eventTypeId` | string |  |
| `attributes.name` | string |  |
| `attributes.registrantsCount` | number |  |
| `attributes.roomLink` | string |  |
| `attributes.startedAt` | number |  |
| `attributes.status` | string |  |
| `attributes.timezone` | string |  |
| `attributes.updatedAt` | number |  |
| `id` | string | ID |
| `type` | string | Type |

## Native endpoint

Through the native Livestorm API, this operation is `GET events/:id/sessions` (base URL `https://api.livestorm.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-event-sessions.md) for the provider-specific parameters and requirements.

