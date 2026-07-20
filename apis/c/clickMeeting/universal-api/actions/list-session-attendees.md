# ClickMeeting: List Session Attendees

Retrieves attendees for a session in ClickMeeting.

```
GET https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/list-session-attendees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickMeeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/list-session-attendees?connectionId=$CONNECTION_ID&room_id=1&session_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "room_id": "1",
  "session_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/list-session-attendees?${params}`, {
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
      "device": "string",
      "email": "ava@example.com",
      "nickname": "Ava Chen",
      "polls": [
        {}
      ],
      "rating": "string",
      "rating_comment": "string",
      "role": "string",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `device` | string | Attendee device/user agent. |
| `email` | string | Attendee email address. |
| `nickname` | string | Attendee nickname. |
| `polls` | array<object> | Poll results captured for the attendee. |
| `rating` | string | Attendee rating. |
| `rating_comment` | string | Attendee rating comment. |
| `role` | string | Attendee role. |
| `uid` | string | Attendee unique identifier. |

## Native endpoint

Through the native ClickMeeting API, this operation is `GET conferences/{{room_id}}/sessions/{{session_id}}/attendees` (base URL `https://api.clickmeeting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-session-attendees.md) for the provider-specific parameters and requirements.

