# ClickMeeting: Update Conference

Updates a conference in ClickMeeting by room ID.

```
PUT https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/update-conference
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickMeeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/update-conference" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "room_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/update-conference', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "room_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `room_id` | number | yes | Conference room identifier. |
| `name` | string | no | Updated room name. |
| `room_type` | list | no | Updated room type. One of: `meeting`, `webinar`. |
| `permanent_room` | boolean | no | Required when changing starts_at or duration. |
| `access_type` | list<number> | no | Updated room access model. One of: `1`, `2`, `3`. |
| `lobby_description` | string | no | Updated lobby message. |
| `lobby_enabled` | boolean | no | Turn the lobby on or off. |
| `starts_at` | date | no | Updated conference start timestamp. |
| `duration` | string | no | Updated duration, for example 1:20 or 0:20. |
| `timezone` | string | no | Updated conference time zone. |
| `skin_id` | number | no | Updated skin identifier. |
| `password` | string | no | Updated room password. |
| `status` | list | no | Activate or deactivate the conference. One of: `active`, `inactive`. |
| `registration.enabled` | boolean | no | Enable or disable registration. |
| `registration.template` | list<number> | no | Updated registration template ID. One of: `1`, `2`, `3`. |

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

## Response

```json
{
  "success": true,
  "data": [
    {
      "conference": {
        "embed_room_url": "https://example.com",
        "id": 1,
        "name": "Ava Chen",
        "permanent_room": true,
        "room_type": "string",
        "room_url": "https://example.com",
        "starts_at": "2026-05-07T12:00:00.000Z",
        "status": "string",
        "updated_at": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conference.embed_room_url` | string | Embeddable conference room URL. |
| `conference.id` | number | Conference room identifier. |
| `conference.name` | string | Conference room name. |
| `conference.permanent_room` | boolean | Whether the room is permanent. |
| `conference.room_type` | string | Conference room type. |
| `conference.room_url` | string | Conference room URL. |
| `conference.starts_at` | date | Conference start timestamp. |
| `conference.status` | string | Conference room status. |
| `conference.updated_at` | date | Conference update timestamp. |

## Native endpoint

Through the native ClickMeeting API, this operation is `PUT conferences/{{room_id}}` (base URL `https://api.clickmeeting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-conference.md) for the provider-specific parameters and requirements.

