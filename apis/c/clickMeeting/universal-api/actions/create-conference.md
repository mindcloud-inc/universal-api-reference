# ClickMeeting: Create Conference

Creates a new conference in ClickMeeting.

```
POST https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/create-conference
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickMeeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/create-conference" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "room_type": "meeting",
  "permanent_room": true,
  "access_type": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/create-conference', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "room_type": "meeting",
    "permanent_room": true,
    "access_type": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Room name shown to attendees. |
| `room_type` | list | yes | Choose whether to create a meeting or webinar room. One of: `meeting`, `webinar`. Default: `meeting`. |
| `permanent_room` | boolean | yes | Use true for a permanent room, false for a scheduled room. |
| `access_type` | list<number> | yes | Choose the room access model. One of: `1`, `2`, `3`. Default: `1`. |
| `custom_room_url_name` | string | no | Optional custom room URL suffix. |
| `lobby_description` | string | no | Optional lobby message shown before the room starts. |
| `lobby_enabled` | boolean | no | Turn the lobby on or off. |
| `starts_at` | date | no | Scheduled conference start timestamp. |
| `duration` | string | no | Conference duration, for example 1:20 or 0:20. |
| `timezone` | string | no | Conference time zone, for example America/New_York. |
| `skin_id` | number | no | Optional room skin identifier. |
| `password` | string | no | Required only for password-protected rooms. |
| `registration.enabled` | boolean | no | Enable or disable attendee registration. |
| `registration.template` | list<number> | no | Optional registration template ID. One of: `1`, `2`, `3`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `settings.show_on_personal_page` | boolean | no | Display the conference on the personal page. |
| `settings.thank_you_emails_enabled` | boolean | no | Send thank-you emails after the conference. |
| `settings.connection_tester_enabled` | boolean | no | Enable the connection tester. |
| `settings.phonegateway_enabled` | boolean | no | Enable dial-in phone gateways. |
| `settings.recorder_autostart_enabled` | boolean | no | Auto-start the recorder. |
| `settings.room_invite_button_enabled` | boolean | no | Show the room invite button. |
| `settings.social_media_sharing_enabled` | boolean | no | Allow social sharing from the room. |
| `settings.connection_status_enabled` | boolean | no | Show attendee connection status. |
| `settings.thank_you_page_url` | string | no | Optional custom thank-you page URL. |
| `settings.encryption_enabled` | boolean | no | Enable end-to-end encryption. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "room": {
        "created_at": "2026-05-07T12:00:00.000Z",
        "embed_room_url": "https://example.com",
        "id": 1,
        "name": "Ava Chen",
        "permanent_room": true,
        "room_type": "string",
        "room_url": "https://example.com",
        "starts_at": "2026-05-07T12:00:00.000Z",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `room.created_at` | date | Conference creation timestamp. |
| `room.embed_room_url` | string | Embeddable conference room URL. |
| `room.id` | number | Created conference room identifier. |
| `room.name` | string | Created conference room name. |
| `room.permanent_room` | boolean | Whether the room is permanent. |
| `room.room_type` | string | Created conference room type. |
| `room.room_url` | string | Created conference room URL. |
| `room.starts_at` | date | Conference start timestamp. |
| `room.status` | string | Created conference room status. |

## Native endpoint

Through the native ClickMeeting API, this operation is `POST conferences` (base URL `https://api.clickmeeting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-conference.md) for the provider-specific parameters and requirements.

