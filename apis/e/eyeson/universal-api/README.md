# <img src="https://images.mindcloud.co/apps/icons/eyeson_1776908646702.png" alt="Eyeson logo" width="28" height="28"> Eyeson: Universal API

Eyeson is a video meeting API for creating and managing rooms, users, media layers, layouts, recordings, snapshots, broadcasts, and related real-time meeting resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eyeson/latest
- **Category:** Communication / Video Communications
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.eyeson.com/
- **Vendor API docs:** https://docs.eyeson.com/docs/rest/eyeson-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Meeting Details](actions/get-meeting-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eyeson/latest/actions/get-meeting-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Meeting

| Action | Method | Description |
| --- | --- | --- |
| [List Current Meetings](actions/list-current-meetings.md) | GET |  |

### Meetings

| Action | Method | Description |
| --- | --- | --- |
| [Create Permalink](actions/create-permalink.md) | POST |  |
| [Delete Permalink](actions/delete-permalink.md) | DELETE |  |
| [End Meeting](actions/end-meeting.md) | DELETE |  |
| [Force Stop Meeting](actions/force-stop-meeting.md) | DELETE |  |
| [Get Meeting Details](actions/get-meeting-details.md) | GET |  |
| [Get Permalink](actions/get-permalink.md) | GET |  |
| [List Permalinks](actions/list-permalinks.md) | GET |  |
| [Lock Meeting](actions/lock-meeting.md) | PUT |  |
| [Set Meeting Layout](actions/set-meeting-layout.md) | PUT |  |
| [Start Meeting](actions/start-meeting.md) | POST |  |
| [Start Permalink Meeting](actions/start-permalink-meeting.md) | POST |  |
| [Update Permalink](actions/update-permalink.md) | PUT |  |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Send Meeting Message](actions/send-meeting-message.md) | POST |  |

### Recordings

| Action | Method | Description |
| --- | --- | --- |
| [Get Recording](actions/get-recording.md) | GET |  |
| [Start Recording](actions/start-recording.md) | POST |  |
| [Stop Recording](actions/stop-recording.md) | PUT |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Add Meeting Layer](actions/add-meeting-layer.md) | POST |  |
| [Delete Meeting Layer](actions/delete-meeting-layer.md) | DELETE |  |
| [Start Broadcast](actions/start-broadcast.md) | POST |  |
| [Start Meeting Playback](actions/start-meeting-playback.md) | POST |  |
| [Stop Broadcast](actions/stop-broadcast.md) | DELETE |  |
| [Stop Meeting Playback](actions/stop-meeting-playback.md) | DELETE |  |
| [Update Broadcast Player URL](actions/update-broadcast-player-url.md) | PUT |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Meeting User](actions/get-meeting-user.md) | GET |  |
| [List Meeting Users](actions/list-meeting-users.md) | GET |  |
| [Register Guest User](actions/register-guest-user.md) | POST |  |
| [Register Permalink Host User](actions/register-permalink-host-user.md) | POST |  |
| [Remove Meeting User](actions/remove-meeting-user.md) | DELETE |  |
| [Remove Permalink Host User](actions/remove-permalink-host-user.md) | DELETE |  |

