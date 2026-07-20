# SignalWire: List Conference Rooms

Retrieves conference rooms from SignalWire.

```
GET https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-conference-rooms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-conference-rooms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-conference-rooms?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "conference_room": {
        "description": "string",
        "display_name": "Ava Chen",
        "enable_room_previews": true,
        "fps": 1,
        "id": "string",
        "join_from": "2026-05-07T12:00:00.000Z",
        "join_until": "2026-05-07T12:00:00.000Z",
        "layout": "string",
        "max_members": 1,
        "meta": {},
        "name": "Ava Chen",
        "prioritize_handraise": true,
        "quality": "string",
        "record_on_start": true,
        "remove_after_seconds_elapsed": 1,
        "remove_at": "2026-05-07T12:00:00.000Z",
        "room_join_video_off": true,
        "sync_audio_video": true,
        "tone_on_entry_and_exit": true,
        "user_join_video_off": true
      },
      "created_at": "2026-05-07T12:00:00.000Z",
      "display_name": "Ava Chen",
      "id": "string",
      "project_id": "string",
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conference_room.description` | string | The descrption of the Conference Room |
| `conference_room.display_name` | string | Display name of the Conference Room |
| `conference_room.enable_room_previews` | boolean | Enables live video room previews for the conference. |
| `conference_room.fps` | number | The frames-per-second (fps) of the participants videos in the conference. |
| `conference_room.id` | string | The unique id of the Conference Room |
| `conference_room.join_from` | date | The time users are allowed to start joining the conference. Joining before this time will result in failure to join the conference. |
| `conference_room.join_until` | date | The time users are allowed to until the conference is locked. Attempting to join the conference after the set time will result in failure to join the conference. |
| `conference_room.layout` | string | The video layout of the conference. |
| `conference_room.max_members` | number | Maximum number of members allowed in the conference room |
| `conference_room.meta` | object | Metadata of the conference. |
| `conference_room.name` | string | The name of the Conference Room |
| `conference_room.prioritize_handraise` | boolean | Indicator if the Conference Room will prioritize showing participants utilizing the hand raised feature. |
| `conference_room.quality` | string | The viudeo quality of the Conference Room. |
| `conference_room.record_on_start` | boolean | Starts recording when the conference starts. |
| `conference_room.remove_after_seconds_elapsed` | number | The amount of time in seconds to remove a particpant from a conference after they join. |
| `conference_room.remove_at` | date | The time to remove all participants from the conference. |
| `conference_room.room_join_video_off` | boolean | Turns the conference video off when the participant joins the room if `true`. |
| `conference_room.sync_audio_video` | boolean | Syncs the participants audio and video. |
| `conference_room.tone_on_entry_and_exit` | boolean | Plays a tone when a participant joins or leaves the conference. |
| `conference_room.user_join_video_off` | boolean | Turns the participants video off when the participant joins the room if `true`. |
| `created_at` | date | Date and time when the resource was created. |
| `display_name` | string | Display name of the Conference Room Fabric Resource |
| `id` | string | Unique ID of the Conference Room. |
| `project_id` | string | Unique ID of the Project. |
| `type` | string | Type of the Fabric Resource |
| `updated_at` | date | Date and time when the resource was updated. |

## Native endpoint

Through the native SignalWire API, this operation is `GET /fabric/resources/conference_rooms` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conference-rooms.md) for the provider-specific parameters and requirements.

