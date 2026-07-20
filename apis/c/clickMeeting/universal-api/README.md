# <img src="https://images.mindcloud.co/apps/icons/click-meeting_1773855848294.png" alt="ClickMeeting logo" width="28" height="28"> ClickMeeting: Universal API

ClickMeeting: Create, host, and manage webinars, meetings, and recordings

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/clickMeeting/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://clickmeeting.com
- **Vendor API docs:** https://dev.clickmeeting.com/api-guide/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Phone Gateways](actions/list-phone-gateways.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/list-phone-gateways?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Generate Access Tokens](actions/generate-access-tokens.md) | POST | Creates access tokens for a conference in ClickMeeting. |
| [List Access Tokens](actions/list-access-tokens.md) | GET | Retrieves access tokens for a conference in ClickMeeting. |

### Chat

| Action | Method | Description |
| --- | --- | --- |
| [Download Chat Archive](actions/download-chat-archive.md) | GET | Downloads a chat archive from ClickMeeting by session ID. |
| [List Chats](actions/list-chats.md) | GET | Retrieves chat archives from ClickMeeting sessions. |

### Conference

| Action | Method | Description |
| --- | --- | --- |
| [Create Conference](actions/create-conference.md) | POST | Creates a new conference in ClickMeeting. |
| [Delete Conference](actions/delete-conference.md) | DELETE | Deletes a conference from ClickMeeting by room ID. |
| [Get Conference](actions/get-conference.md) | GET | Retrieves a conference from ClickMeeting by room ID. |
| [List Conferences](actions/list-conferences.md) | GET | Retrieves conferences from ClickMeeting by active or inactive status. |
| [Update Conference](actions/update-conference.md) | PUT | Updates a conference in ClickMeeting by room ID. |

### Conference Auto-login

| Action | Method | Description |
| --- | --- | --- |
| [Generate Conference Auto-Login URL](actions/generate-conference-auto-login-url.md) | POST | Creates an auto-login URL for a conference in ClickMeeting. |

### Conference Invitation

| Action | Method | Description |
| --- | --- | --- |
| [Send Conference Invitation](actions/send-conference-invitation.md) | POST | Sends a conference invitation email from ClickMeeting. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE | Deletes a file from ClickMeeting by file ID. |
| [Download File](actions/download-file.md) | GET | Downloads a file from ClickMeeting by file ID. |
| [Get File](actions/get-file.md) | GET | Retrieves a file from ClickMeeting by file ID. |
| [List Conference Files](actions/list-conference-files.md) | GET | Retrieves files for a conference in ClickMeeting. |
| [List Files](actions/list-files.md) | GET | Retrieves file library files from ClickMeeting. |
| [Upload Conference File](actions/upload-conference-file.md) | POST | Creates a conference file in ClickMeeting. |
| [Upload File](actions/upload-file.md) | POST | Creates a file in the ClickMeeting file library. |

### Phone Gateway

| Action | Method | Description |
| --- | --- | --- |
| [List Phone Gateways](actions/list-phone-gateways.md) | GET | Retrieves available phone gateways from ClickMeeting. |

### Recording

| Action | Method | Description |
| --- | --- | --- |
| [Delete All Conference Recordings](actions/delete-all-conference-recordings.md) | DELETE | Deletes all conference recordings from ClickMeeting. |
| [Delete Recording](actions/delete-recording.md) | DELETE | Deletes a recording from ClickMeeting by recording ID. |
| [List Conference Recordings](actions/list-conference-recordings.md) | GET | Retrieves recordings for a conference in ClickMeeting. |

### Registration

| Action | Method | Description |
| --- | --- | --- |
| [List Conference Registrations](actions/list-conference-registrations.md) | GET | Retrieves conference registrations from ClickMeeting by registration status. |
| [List Session Registrations](actions/list-session-registrations.md) | GET | Retrieves registrations for a session in ClickMeeting. |
| [Register Conference Participant](actions/register-conference-participant.md) | POST | Creates a conference participant registration in ClickMeeting. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Get Conference Session](actions/get-conference-session.md) | GET | Retrieves a conference session from ClickMeeting. |
| [List Conference Sessions](actions/list-conference-sessions.md) | GET | Retrieves sessions for a conference in ClickMeeting. |

### Session Attendee

| Action | Method | Description |
| --- | --- | --- |
| [List Session Attendees](actions/list-session-attendees.md) | GET | Retrieves attendees for a session in ClickMeeting. |

### Session Report

| Action | Method | Description |
| --- | --- | --- |
| [Generate Session PDF Report](actions/generate-session-pdf-report.md) | GET | Generates a session PDF report in ClickMeeting. |

### Time Zone

| Action | Method | Description |
| --- | --- | --- |
| [List Time Zones](actions/list-time-zones.md) | GET | Retrieves available time zones from ClickMeeting. |

