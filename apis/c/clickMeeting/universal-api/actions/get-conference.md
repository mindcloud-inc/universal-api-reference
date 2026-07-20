# ClickMeeting: Get Conference

Retrieves a conference from ClickMeeting by room ID.

```
GET https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/get-conference
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickMeeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/get-conference?connectionId=$CONNECTION_ID&room_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "room_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/get-conference?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "conference": {
        "created_at": "2026-05-07T12:00:00.000Z",
        "embed_room_url": "https://example.com",
        "id": 1,
        "name": "Ava Chen",
        "permanent_room": true,
        "registration_enabled": 1,
        "room_type": "string",
        "room_url": "https://example.com",
        "status": "string",
        "timezone": "string",
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
| `conference.created_at` | date | Conference creation timestamp. |
| `conference.embed_room_url` | string | Embeddable conference room URL. |
| `conference.id` | number | Conference room identifier. |
| `conference.name` | string | Conference room name. |
| `conference.permanent_room` | boolean | Whether the room is permanent. |
| `conference.registration_enabled` | number | Registration toggle reported by the API. |
| `conference.room_type` | string | Conference room type. |
| `conference.room_url` | string | Conference room URL. |
| `conference.status` | string | Conference room status. |
| `conference.timezone` | string | Conference time zone. |
| `conference.updated_at` | date | Conference update timestamp. |

## Native endpoint

Through the native ClickMeeting API, this operation is `GET conferences/{{room_id}}` (base URL `https://api.clickmeeting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conference.md) for the provider-specific parameters and requirements.

