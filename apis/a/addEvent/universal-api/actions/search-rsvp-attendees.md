# AddEvent: Search RSVP attendees



```
GET https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/search-rsvp-attendees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AddEvent `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/search-rsvp-attendees?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/search-rsvp-attendees?${params}`, {
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
| `calendarIds[]` | array<string> | no | Limit results to specific calendars. Accepts multiple values in one string, delimited by `,`. |
| `eventIds[]` | array<string> | no | Limit results to specific events. Accepts multiple values in one string, delimited by `,`. |
| `attending[]` | array<string> | no | Filter RSVP attendees by response status. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attending": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "eventId": "string",
      "geoLocation": {
        "city": "string",
        "country": "string",
        "ip": "string",
        "location": "string",
        "postal": "string",
        "region": "string"
      },
      "id": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "rsvpFormData": {
        "name": "Ava Chen"
      },
      "rsvpFormLabels": {
        "email": "ava@example.com",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attending` | string | Attendee RSVP response. |
| `created` | date | Attendee creation timestamp. |
| `email` | string | Attendee email address. |
| `eventId` | string | Associated event ID. |
| `geoLocation.city` | string |  |
| `geoLocation.country` | string |  |
| `geoLocation.ip` | string |  |
| `geoLocation.location` | string |  |
| `geoLocation.postal` | string |  |
| `geoLocation.region` | string |  |
| `id` | string | Unique identifier of the RSVP attendee. |
| `modified` | date | Attendee last modified timestamp. |
| `rsvpFormData.name` | string |  |
| `rsvpFormLabels.email` | string |  |
| `rsvpFormLabels.name` | string |  |

## Native endpoint

Through the native AddEvent API, this operation is `GET /rsvps` (base URL `https://api.addevent.com/calevent/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-rsvp-attendees.md) for the provider-specific parameters and requirements.

