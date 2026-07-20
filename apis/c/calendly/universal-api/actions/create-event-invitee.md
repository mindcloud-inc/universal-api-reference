# Calendly: Create Event Invitee

Creates an event invitee in Calendly.

```
POST https://connect.mindcloud.co/v1/universal/calendly/latest/actions/create-event-invitee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calendly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/calendly/latest/actions/create-event-invitee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "event_type": "https://api.calendly.com/event_types/8d38b11a-269e-4878-ab4a-12048b63906d",
  "start_time": "2026-03-03T15:00:00Z",
  "end_time": "2026-03-03T15:30:00Z",
  "invitee": {},
  "invitee.name": "Test Invitee",
  "invitee.email": "apps+invitee@mindcloud.co",
  "location": {},
  "location.kind": "google_conference"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/calendly/latest/actions/create-event-invitee', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "event_type": "https://api.calendly.com/event_types/8d38b11a-269e-4878-ab4a-12048b63906d",
    "start_time": "2026-03-03T15:00:00Z",
    "end_time": "2026-03-03T15:30:00Z",
    "invitee": {},
    "invitee.name": "Test Invitee",
    "invitee.email": "apps+invitee@mindcloud.co",
    "location": {},
    "location.kind": "google_conference"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `event_type` | string | yes | Event type URI. Default: `https://api.calendly.com/event_types/8d38b11a-269e-4878-ab4a-12048b63906d`. |
| `start_time` | date | yes | Invitee start time (ISO-8601). Default: `2026-03-03T15:00:00Z`. |
| `end_time` | date | yes | Invitee end time (ISO-8601). Default: `2026-03-03T15:30:00Z`. |
| `invitee` | object | yes |  |
| `invitee.name` | string | yes | Invitee full name. Default: `Test Invitee`. |
| `invitee.email` | string | yes | Invitee email. Default: `apps+invitee@mindcloud.co`. |
| `location` | object | yes |  |
| `location.kind` | string | yes | Location kind configured on the event type (for example google_conference). Default: `google_conference`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invitee.timezone` | string | no | Invitee timezone. Default: `UTC`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Calendly API returns.

## Native endpoint

Through the native Calendly API, this operation is `POST /invitees` (base URL `https://api.calendly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event-invitee.md) for the provider-specific parameters and requirements.

