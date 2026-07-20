# Dialpad: Native API Reference

A consolidated summary of Dialpad's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developers.dialpad.com/reference
- **OpenAPI specification:** https://dialpad.com/static/openapi/platform-v1.0.json
- **API base URL:** `https://dialpad.com/api/v2`

## Authentication

### OAuth2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://dialpad.com/oauth2/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://dialpad.com/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `recordings_export message_content_export message_content_export:all screen_pop calls:list fax_message change_log offline_access`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://dialpad.com/oauth2/token.

[Official authentication documentation](https://developers.dialpad.com/docs/oauth)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Channel](actions/create-channel.md) | `POST /channels` | [docs](https://developers.dialpad.com/reference/channelspost) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://developers.dialpad.com/reference/contactscreate) |
| [Create Meeting](actions/create-meeting.md) | `POST /meetings` | [docs](https://developers.dialpad.com/reference/meetingscreate) |
| [Create or Update Contact](actions/create-or-update-contact.md) | `PUT /contacts` | [docs](https://developers.dialpad.com/reference/contactscreate_with_uid) |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://developers.dialpad.com/reference/userscreate) |
| [Get Call](actions/get-call.md) | `GET /call/:id` | [docs](https://developers.dialpad.com/reference/callget_call_info) |
| [Get Call AI Recap](actions/get-call-ai-recap.md) | `GET /call/:id/ai_recap` | [docs](https://developers.dialpad.com/reference/callai_recap) |
| [Get Call Transcript](actions/get-call-transcript.md) | `GET /transcripts/:call_id` | [docs](https://developers.dialpad.com/reference/transcriptsget) |
| [Get Channel](actions/get-channel.md) | `GET /channels/:id` | [docs](https://developers.dialpad.com/reference/channelsget) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id` | [docs](https://developers.dialpad.com/reference/contactsget) |
| [Get Current User](actions/get-current-user.md) | `GET /users/me` | [docs](https://developers.dialpad.com/reference/usersget) |
| [Get Meeting](actions/get-meeting.md) | `GET /meetings/:id` | [docs](https://developers.dialpad.com/reference/meetingsget) |
| [Get Office](actions/get-office.md) | `GET /offices/:id` | [docs](https://developers.dialpad.com/reference/officesget) |
| [Get User](actions/get-user.md) | `GET /users/:id` | [docs](https://developers.dialpad.com/reference/usersget) |
| [Initiate Call](actions/initiate-call.md) | `POST /users/:id/initiate_call` | [docs](https://developers.dialpad.com/reference/usersinitiate_call) |
| [List Call Centers](actions/list-call-centers.md) | `GET /callcenters` | [docs](https://developers.dialpad.com/reference/callcenterslist) |
| [List Calls](actions/list-calls.md) | `GET /call` | [docs](https://developers.dialpad.com/reference/calllist) |
| [List Channel Members](actions/list-channel-members.md) | `GET /channels/:id/members` | [docs](https://developers.dialpad.com/reference/channelsmemberslist) |
| [List Channels](actions/list-channels.md) | `GET /channels` | [docs](https://developers.dialpad.com/reference/channelslist) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://developers.dialpad.com/reference/contactslist) |
| [List Departments](actions/list-departments.md) | `GET /departments` | [docs](https://developers.dialpad.com/reference/departmentslist) |
| [List Meetings](actions/list-meetings.md) | `GET /meetings` | [docs](https://developers.dialpad.com/reference/meetingslist) |
| [List Numbers](actions/list-numbers.md) | `GET /numbers` | [docs](https://developers.dialpad.com/reference/numberslist) |
| [List Offices](actions/list-offices.md) | `GET /offices` | [docs](https://developers.dialpad.com/reference/officeslist) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://developers.dialpad.com/reference/userslist) |
| [Send SMS](actions/send-sms.md) | `POST /sms` | [docs](https://developers.dialpad.com/reference/smssend) |
| [Transfer Call](actions/transfer-call.md) | `POST /call/:id/transfer` | [docs](https://developers.dialpad.com/reference/calltransfer_call) |
| [Update Contact](actions/update-contact.md) | `PATCH /contacts/:id` | [docs](https://developers.dialpad.com/reference/contactsupdate) |
| [Update User](actions/update-user.md) | `PATCH /users/:id` | [docs](https://developers.dialpad.com/reference/usersupdate) |
| [Update User Status](actions/update-user-status.md) | `PATCH /users/:id/status` | [docs](https://developers.dialpad.com/reference/usersupdate_status) |
