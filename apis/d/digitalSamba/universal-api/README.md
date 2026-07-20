# <img src="https://images.mindcloud.co/apps/icons/digital-samba_1776700208206.png" alt="Digital Samba logo" width="28" height="28"> Digital Samba: Universal API

Digital Samba Embedded provides video conferencing rooms, sessions, participants, recordings, roles, libraries, live usage, statistics, and webhooks through REST APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/digitalSamba/latest
- **Category:** Communication / Video Communications
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.digitalsamba.com
- **Vendor API docs:** https://docs.digitalsamba.com/reference/rest-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get all team rooms](actions/get-all-team-rooms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-all-team-rooms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Default Room Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get default room settings](actions/get-default-room-settings.md) | GET | Retrieves default room settings from Digital Samba. |
| [Update default room settings](actions/update-default-room-settings.md) | PUT | Updates default room settings in Digital Samba. |

### Libraries

| Action | Method | Description |
| --- | --- | --- |
| [Get available libraries for the team](actions/get-available-libraries-for-the-team.md) | GET | Retrieves team libraries from Digital Samba. |
| [Get available library files](actions/get-available-library-files.md) | GET | Retrieves library files from Digital Samba. |
| [Get the specified library hierarchy](actions/get-the-specified-library-hierarchy.md) | GET | Retrieves a library hierarchy from Digital Samba. |

### Live

| Action | Method | Description |
| --- | --- | --- |
| [Get rooms with live participants count](actions/get-rooms-with-live-participants-count.md) | GET | Retrieves live participant counts for rooms in Digital Samba. |
| [Get rooms with live participants data](actions/get-rooms-with-live-participants-data.md) | GET | Retrieves live participant data for rooms in Digital Samba. |

### Participants

| Action | Method | Description |
| --- | --- | --- |
| [Get all participants](actions/get-all-participants.md) | GET | Retrieves participants from Digital Samba. |
| [Get all room participants](actions/get-all-room-participants.md) | GET | Retrieves room participants from Digital Samba. |
| [Get all session participants](actions/get-all-session-participants.md) | GET | Retrieves session participants from Digital Samba. |
| [Get participant statistics](actions/get-participant-statistics.md) | GET | Retrieves participant statistics from Digital Samba. |

### Permissions

| Action | Method | Description |
| --- | --- | --- |
| [Get available permissions for roles](actions/get-available-permissions-for-roles.md) | GET | Retrieves role permissions from Digital Samba. |

### Recordings

| Action | Method | Description |
| --- | --- | --- |
| [Archive recording](actions/archive-recording.md) | PUT | Updates a recording to archived in Digital Samba. |
| [Download the specified recording](actions/download-the-specified-recording.md) | GET | Retrieves a recording download from Digital Samba. |
| [Get all team recordings](actions/get-all-team-recordings.md) | GET | Retrieves team recordings from Digital Samba. |
| [Get archived team recordings](actions/get-archived-team-recordings.md) | GET | Retrieves archived team recordings from Digital Samba. |
| [Get bookmarks](actions/get-bookmarks.md) | GET | Retrieves recording bookmarks from Digital Samba. |
| [Get the specified recording](actions/get-the-specified-recording.md) | GET | Retrieves a recording from Digital Samba. |
| [Unarchive recording](actions/unarchive-recording.md) | PUT | Updates a recording to unarchived in Digital Samba. |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [Create a new role](actions/create-a-new-role.md) | POST | Creates a new role in Digital Samba. |
| [Get available roles for the team](actions/get-available-roles-for-the-team.md) | GET | Retrieves team roles from Digital Samba. |
| [Get the specified role](actions/get-the-specified-role.md) | GET | Retrieves a role from Digital Samba. |
| [Update the specified role](actions/update-the-specified-role.md) | PUT | Updates an existing role in Digital Samba. |

### Rooms

| Action | Method | Description |
| --- | --- | --- |
| [Create a new room](actions/create-a-new-room.md) | POST | Creates a new room in Digital Samba. |
| [Create a question in the room](actions/create-a-question-in-the-room.md) | POST | Creates a room question in Digital Samba. |
| [Create room token](actions/create-room-token.md) | POST | Creates a room access token in Digital Samba. |
| [Delete room](actions/delete-room.md) | DELETE | Deletes an existing room from Digital Samba. |
| [Get all team rooms](actions/get-all-team-rooms.md) | GET | Retrieves team rooms from Digital Samba. |
| [Get chat messages](actions/get-chat-messages.md) | GET | Retrieves room chat messages from Digital Samba. |
| [Get questions and answers](actions/get-questions-and-answers.md) | GET | Retrieves room questions and answers from Digital Samba. |
| [Get room transcripts](actions/get-room-transcripts.md) | GET | Retrieves room transcripts from Digital Samba. |
| [Get the specified room](actions/get-the-specified-room.md) | GET | Retrieves a room from Digital Samba. |
| [Send chat message](actions/send-chat-message.md) | POST | Creates a room chat message in Digital Samba. |
| [Update room](actions/update-room.md) | PUT | Updates an existing room in Digital Samba. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Get all room sessions](actions/get-all-room-sessions.md) | GET | Retrieves room sessions from Digital Samba. |
| [Get all sessions](actions/get-all-sessions.md) | GET | Retrieves sessions from Digital Samba. |
| [Get session statistics](actions/get-session-statistics.md) | GET | Retrieves session statistics from Digital Samba. |
| [Get session summary](actions/get-session-summary.md) | GET | Retrieves a session summary from Digital Samba. |
| [Get session transcripts](actions/get-session-transcripts.md) | GET | Retrieves session transcripts from Digital Samba. |

### Webhooks

| Action | Method | Description |
| --- | --- | --- |
| [Get webhooks for the team](actions/get-webhooks-for-the-team.md) | GET | Retrieves team webhooks from Digital Samba. |

