# Create Conference Room with SignalWire

Creates a new conference room in SignalWire.

## Endpoint

- **Method:** `POST`
- **Path:** `/fabric/resources/conference_rooms`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Create Conference Room](https://signalwire.com/docs/apis/rest/conference-rooms/create-conference-room)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the Conference Room |
| `display_name` | body | `string` | no | Display name of the Conference Room |
| `description` | body | `string` | no | The descrption of the Conference Room |
| `join_from` | body | `date` | no | The time users are allowed to start joining the conference. Joining before this time will result in failure to join the conference. |
| `join_until` | body | `date` | no | The time users are allowed to until the conference is locked. Attempting to join the conference after the set time will result in failure to join the conference. |
| `max_members` | body | `number` | no | Maximum number of members allowed in the conference room |
| `quality` | body | `string` | no | The viudeo quality of the Conference Room. |
| `remove_at` | body | `date` | no | The time to remove all participants from the conference. |
| `remove_after_seconds_elapsed` | body | `number` | no | The amount of time in seconds to remove a particpant from a conference after they join. |
| `layout` | body | `string` | no | The video layout of the conference. |
| `record_on_start` | body | `boolean` | no | Starts recording when the conference starts. |
| `enable_room_previews` | body | `boolean` | yes | Enables live video room previews for the conference. |
| `meta` | body | `object` | no | Metadata of the conference. |
| `sync_audio_video` | body | `boolean` | no | Syncs the participants audio and video. |
| `tone_on_entry_and_exit` | body | `boolean` | no | Plays a tone when a participant joins or leaves the conference. |
| `room_join_video_off` | body | `boolean` | no | Turns the conference video off when the participant joins the room if `true`. |
| `user_join_video_off` | body | `boolean` | no | Turns the participants video off when the participant joins the room if `true`. |
