# SignalWire: Update Conference Room

Updates an existing conference room in SignalWire.

```
PUT https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/update-conference-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/update-conference-room" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "enableRoomPreviews": true,
  "syncAudioVideo": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/update-conference-room', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "enableRoomPreviews": true,
    "syncAudioVideo": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Unique ID of a Conference Room. |
| `name` | string | no | The name of the Conference Room |
| `displayName` | string | no | Display name of the Conference Room |
| `description` | string | no | The descrption of the Conference Room |
| `joinFrom` | date | no | The time users are allowed to start joining the conference. Joining before this time will result in failure to join the conference. |
| `joinUntil` | date | no | The time users are allowed to until the conference is locked. Attempting to join the conference after the set time will result in failure to join the conference. |
| `maxMembers` | number | no | Maximum number of members allowed in the conference room |
| `quality` | string | no | The viudeo quality of the Conference Room. |
| `removeAt` | date | no | The time to remove all participants from the conference. |
| `removeAfterSecondsElapsed` | number | no | The amount of time in seconds to remove a particpant from a conference after they join. |
| `layout` | string | no | The video layout of the conference. |
| `recordOnStart` | boolean | no | Starts recording when the conference starts. |
| `enableRoomPreviews` | boolean | yes | Enables live video room previews for the conference. |
| `meta` | object | no | Metadata of the conference. |
| `syncAudioVideo` | boolean | yes | Syncs the participants audio and video. |
| `toneOnEntryAndExit` | boolean | no | Plays a tone when a participant joins or leaves the conference. |
| `roomJoinVideoOff` | boolean | no | Turns the conference video off when the participant joins the room if `true`. |
| `userJoinVideoOff` | boolean | no | Turns the participants video off when the participant joins the room if `true`. |

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

Through the native SignalWire API, this operation is `PUT /fabric/resources/conference_rooms/{id}` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-conference-room.md) for the provider-specific parameters and requirements.

