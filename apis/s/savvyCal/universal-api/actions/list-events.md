# SavvyCal: List Events



```
GET https://connect.mindcloud.co/v1/universal/savvyCal/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SavvyCal `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/savvyCal/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/savvyCal/latest/actions/list-events?${params}`, {
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
| `state` | string | no |  |
| `period` | string | no |  |
| `from` | date | no |  |
| `until` | date | no |  |
| `direction` | string | no |  |
| `attendance` | string | no |  |
| `link` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalInfo": "string",
      "attendees": [
        {
          "displayName": "Ava Chen",
          "email": "ava@example.com",
          "id": "string",
          "isOrganizer": true,
          "responseStatus": "string"
        }
      ],
      "bufferAfter": 1,
      "bufferBefore": 1,
      "conferencing": {
        "joinUrl": "https://example.com",
        "meetingId": "string",
        "type": "string"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "duration": 1,
      "endAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isGroupSession": true,
      "link": {
        "id": "https://example.com",
        "name": "https://example.com",
        "slug": "https://example.com"
      },
      "location": "string",
      "maximumGroupSize": 1,
      "organizer": {
        "displayName": "Ava Chen",
        "email": "ava@example.com",
        "id": "string"
      },
      "payment": {
        "amountTotal": 1,
        "state": "string"
      },
      "scheduler": {
        "displayName": "Ava Chen",
        "email": "ava@example.com",
        "id": "string"
      },
      "scope": {
        "id": "string",
        "name": "Ava Chen",
        "slug": "string"
      },
      "startAt": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "summary": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalInfo` | string | Additional event information. |
| `attendees[].displayName` | string | Attendee display name. |
| `attendees[].email` | string | Attendee email address. |
| `attendees[].id` | string | Attendee identifier. |
| `attendees[].isOrganizer` | boolean | Whether the attendee is the organizer. |
| `attendees[].responseStatus` | string | Attendee response status. |
| `bufferAfter` | number | Buffer time after the event. |
| `bufferBefore` | number | Buffer time before the event. |
| `conferencing.joinUrl` | string | Conferencing join URL. |
| `conferencing.meetingId` | string | Conferencing meeting identifier. |
| `conferencing.type` | string | Conferencing provider type. |
| `createdAt` | date | When the event was created. |
| `description` | string | Event description. |
| `duration` | number | Event duration in minutes. |
| `endAt` | date | Event end time. |
| `id` | string | Unique event identifier. |
| `isGroupSession` | boolean | Whether the event is a group session. |
| `link.id` | string | Associated link identifier. |
| `link.name` | string | Associated link name. |
| `link.slug` | string | Associated link slug. |
| `location` | string | Location description. |
| `maximumGroupSize` | number | Maximum group size. |
| `organizer.displayName` | string | Organizer display name. |
| `organizer.email` | string | Organizer email address. |
| `organizer.id` | string | Organizer identifier. |
| `payment.amountTotal` | number | Total payment amount. |
| `payment.state` | string | Payment state. |
| `scheduler.displayName` | string | Scheduler display name. |
| `scheduler.email` | string | Scheduler email address. |
| `scheduler.id` | string | Scheduler identifier. |
| `scope.id` | string | Associated scope identifier. |
| `scope.name` | string | Associated scope name. |
| `scope.slug` | string | Associated scope slug. |
| `startAt` | date | Event start time. |
| `state` | string | Current event state. |
| `summary` | string | Event title or summary. |
| `url` | string | Public event URL. |

## Native endpoint

Through the native SavvyCal API, this operation is `GET /v1/events` (base URL `https://api.savvycal.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

