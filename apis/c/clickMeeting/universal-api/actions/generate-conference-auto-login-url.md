# ClickMeeting: Generate Conference Auto-Login URL

Creates an auto-login URL for a conference in ClickMeeting.

```
POST https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/generate-conference-auto-login-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickMeeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/generate-conference-auto-login-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "room_id": 1,
  "email": "ava@example.com",
  "nickname": "Ava Chen",
  "role": "listener"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/generate-conference-auto-login-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "room_id": 1,
    "email": "ava@example.com",
    "nickname": "Ava Chen",
    "role": "listener"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `room_id` | number | yes | Conference room identifier. |
| `email` | string | yes | Attendee email address. |
| `nickname` | string | yes | Attendee nickname. |
| `role` | list | yes | Conference role for the generated auto-login link. One of: `guest_speaker`, `host`, `listener`, `moderator`, `presenter`. Default: `listener`. |
| `password` | string | no | Room password when access_type=2. |
| `token` | string | no | Access token when access_type=3. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autologin_hash": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autologin_hash` | string | Auto-login hash that can be appended to the room URL. |

## Native endpoint

Through the native ClickMeeting API, this operation is `POST conferences/{{room_id}}/room/autologin_hash` (base URL `https://api.clickmeeting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-conference-auto-login-url.md) for the provider-specific parameters and requirements.

