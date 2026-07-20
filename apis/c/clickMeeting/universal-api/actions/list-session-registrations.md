# ClickMeeting: List Session Registrations

Retrieves registrations for a session in ClickMeeting.

```
GET https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/list-session-registrations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickMeeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/list-session-registrations?connectionId=$CONNECTION_ID&room_id=1&session_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "room_id": "1",
  "session_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/list-session-registrations?${params}`, {
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
| `room_id` | number | yes | Conference room identifier. |
| `session_id` | number | yes | Session identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "fields": {},
      "id": 1,
      "registration_confirmed": "string",
      "registration_date": "2026-05-07T12:00:00.000Z",
      "session_id": 1,
      "visitor_nickname": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Registrant email address. |
| `fields` | object | Registration field values. |
| `id` | number | Registration identifier. |
| `registration_confirmed` | string | Registration confirmation state. |
| `registration_date` | date | Registration timestamp. |
| `session_id` | number | Session identifier. |
| `visitor_nickname` | string | Registrant nickname. |

## Native endpoint

Through the native ClickMeeting API, this operation is `GET conferences/{{room_id}}/sessions/{{session_id}}/registrations` (base URL `https://api.clickmeeting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-session-registrations.md) for the provider-specific parameters and requirements.

