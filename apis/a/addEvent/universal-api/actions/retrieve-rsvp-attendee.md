# AddEvent: Retrieve RSVP attendee



```
GET https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/retrieve-rsvp-attendee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AddEvent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/retrieve-rsvp-attendee?connectionId=$CONNECTION_ID&attendeeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "attendeeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/retrieve-rsvp-attendee?${params}`, {
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
| `attendeeId` | string | yes | Unique identifier for the RSVP attendee. |

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

Through the native AddEvent API, this operation is `GET /rsvps/:attendee_id` (base URL `https://api.addevent.com/calevent/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-rsvp-attendee.md) for the provider-specific parameters and requirements.

