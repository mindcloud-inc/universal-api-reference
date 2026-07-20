# ClickMeeting: Native API Reference

A consolidated summary of ClickMeeting's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://dev.clickmeeting.com/api-guide/
- **API base URL:** `https://api.clickmeeting.com/v1`

## Authentication

### API Key

Use a ClickMeeting API key sent in the X-Api-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://dev.clickmeeting.com/api-guide/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Conference](actions/create-conference.md) | `POST conferences` | [docs](https://dev.clickmeeting.com/api-doc/#post_conferences) |
| [Delete All Conference Recordings](actions/delete-all-conference-recordings.md) | `DELETE conferences/{{room_id}}/recordings` | [docs](https://dev.clickmeeting.com/api-doc/#delete_recordings) |
| [Delete Conference](actions/delete-conference.md) | `DELETE conferences/{{room_id}}` | [docs](https://dev.clickmeeting.com/api-doc/#delete_conferences_by_room_id) |
| [Delete File](actions/delete-file.md) | `DELETE file-library/{{file_id}}` | [docs](https://dev.clickmeeting.com/api-doc/#delete_file_library) |
| [Delete Recording](actions/delete-recording.md) | `DELETE conferences/{{room_id}}/recordings/{{recording_id}}` | [docs](https://dev.clickmeeting.com/api-doc/#delete_recording) |
| [Download Chat Archive](actions/download-chat-archive.md) | `GET chats/{{session_id}}` | [docs](https://dev.clickmeeting.com/api-doc/#get_chat) |
| [Download File](actions/download-file.md) | `GET file-library/{{file_id}}/download` | [docs](https://dev.clickmeeting.com/api-doc/#get_file_library_download) |
| [Generate Access Tokens](actions/generate-access-tokens.md) | `POST conferences/{{room_id}}/tokens` | [docs](https://dev.clickmeeting.com/api-doc/#post_tokens) |
| [Generate Conference Auto-Login URL](actions/generate-conference-auto-login-url.md) | `POST conferences/{{room_id}}/room/autologin_hash` | [docs](https://dev.clickmeeting.com/api-doc/#post_autologin_hash) |
| [Generate Session PDF Report](actions/generate-session-pdf-report.md) | `GET conferences/{{room_id}}/sessions/{{session_id}}/generate-pdf/{{lang}}` | [docs](https://dev.clickmeeting.com/api-doc/#get_generate_pdf) |
| [Get Conference](actions/get-conference.md) | `GET conferences/{{room_id}}` | [docs](https://dev.clickmeeting.com/api-doc/#get_conferences_by_room_id) |
| [Get Conference Session](actions/get-conference-session.md) | `GET conferences/{{room_id}}/sessions/{{session_id}}` | [docs](https://dev.clickmeeting.com/api-doc/#get_session) |
| [Get File](actions/get-file.md) | `GET file-library/{{file_id}}` | [docs](https://dev.clickmeeting.com/api-doc/#get_file_library_file) |
| [List Access Tokens](actions/list-access-tokens.md) | `GET conferences/{{room_id}}/tokens` | [docs](https://dev.clickmeeting.com/api-doc/#get_tokens) |
| [List Chats](actions/list-chats.md) | `GET chats` | [docs](https://dev.clickmeeting.com/api-doc/#get_chats) |
| [List Conference Files](actions/list-conference-files.md) | `GET file-library/conferences/{{room_id}}` | [docs](https://dev.clickmeeting.com/api-doc/#get_file_library_by_conference) |
| [List Conference Recordings](actions/list-conference-recordings.md) | `GET conferences/{{room_id}}/recordings` | [docs](https://dev.clickmeeting.com/api-doc/#get_recordings) |
| [List Conference Registrations](actions/list-conference-registrations.md) | `GET conferences/{{room_id}}/registrations/{{status}}` | [docs](https://dev.clickmeeting.com/api-doc/#get_registrations) |
| [List Conference Sessions](actions/list-conference-sessions.md) | `GET conferences/{{room_id}}/sessions` | [docs](https://dev.clickmeeting.com/api-doc/#get_sessions) |
| [List Conferences](actions/list-conferences.md) | `GET conferences/{{status}}` | [docs](https://dev.clickmeeting.com/api-doc/#get_conferences) |
| [List Files](actions/list-files.md) | `GET file-library` | [docs](https://dev.clickmeeting.com/api-doc/#get_file_library) |
| [List Phone Gateways](actions/list-phone-gateways.md) | `GET phone_gateways` | [docs](https://dev.clickmeeting.com/api-doc/#get_phone_gateway) |
| [List Session Attendees](actions/list-session-attendees.md) | `GET conferences/{{room_id}}/sessions/{{session_id}}/attendees` | [docs](https://dev.clickmeeting.com/api-doc/#get_session_attendees) |
| [List Session Registrations](actions/list-session-registrations.md) | `GET conferences/{{room_id}}/sessions/{{session_id}}/registrations` | [docs](https://dev.clickmeeting.com/api-doc/#get_session_registrations) |
| [List Time Zones](actions/list-time-zones.md) | `GET time_zone_list` | [docs](https://dev.clickmeeting.com/api-doc/#get_time_zone_list) |
| [Register Conference Participant](actions/register-conference-participant.md) | `POST conferences/{{room_id}}/registration` | [docs](https://dev.clickmeeting.com/api-doc/#post_registration) |
| [Send Conference Invitation](actions/send-conference-invitation.md) | `POST conferences/{{room_id}}/invitation/email/{{lang}}` | [docs](https://dev.clickmeeting.com/api-doc/#post_invite_email) |
| [Update Conference](actions/update-conference.md) | `PUT conferences/{{room_id}}` | [docs](https://dev.clickmeeting.com/api-doc/#put_conferences_by_room_id) |
| [Upload Conference File](actions/upload-conference-file.md) | `POST file-library/conferences/{{room_id}}` | [docs](https://dev.clickmeeting.com/api-doc/#post_file_library_by_conference) |
| [Upload File](actions/upload-file.md) | `POST file-library` | [docs](https://dev.clickmeeting.com/api-doc/#post_file_library) |
