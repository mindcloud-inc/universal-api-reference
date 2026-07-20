# Cisco Webex Meetings: Native API Reference

A consolidated summary of Cisco Webex Meetings's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://developer.webex.com/meeting/docs/getting-started
- **API base URL:** `https://webexapis.com/v1`

## Authentication

### OAuth2

Connect Cisco Webex Meetings with an OAuth2 integration.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://webexapis.com/v1/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://webexapis.com/v1/access_token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `meeting:schedules_read meeting:schedules_write meeting:participants_read meeting:participants_write meeting:recordings_read meeting:recordings_write meeting:transcripts_read meeting:summaries_read meeting:summaries_write meeting:preferences_read meeting:preferences_write meeting:controls_read meeting:controls_write`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://webexapis.com/v1/access_token.

[Official authentication documentation](https://developer.webex.com/create/docs/authentication)

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create a Meeting](actions/create-meeting.md) | `POST /meetings` | [docs](https://developer.webex.com/docs/api/v1/meetings/create-a-meeting) |
| [Delete a Meeting](actions/delete-meeting.md) | `DELETE /meetings/:meetingId` | [docs](https://developer.webex.com/docs/api/v1/meetings/delete-a-meeting) |
| [Delete a Recording](actions/delete-recording.md) | `DELETE /recordings/:recordingId` | [docs](https://developer.webex.com/docs/api/v1/recordings/delete-a-recording) |
| [Delete a Summary](actions/delete-summary.md) | `DELETE /meetingSummaries/:summaryId` | [docs](https://developer.webex.com/docs/api/v1/meeting-summaries/delete-a-summary) |
| [Download a Meeting Transcript](actions/download-meeting-transcript.md) | `GET /meetingTranscripts/:transcriptId/download` | [docs](https://developer.webex.com/docs/api/v1/meeting-transcripts/download-a-meeting-transcript) |
| [Get a Meeting](actions/get-meeting.md) | `GET /meetings/:meetingId` | [docs](https://developer.webex.com/meeting/docs/api/v1/meetings/get-a-meeting) |
| [Get Recording Details](actions/get-recording-details.md) | `GET /recordings/:recordingId` | [docs](https://developer.webex.com/docs/api/v1/recordings/get-recording-details) |
| [List Meeting Transcripts](actions/list-meeting-transcripts.md) | `GET /meetingTranscripts` | [docs](https://developer.webex.com/docs/api/v1/meeting-transcripts/list-meeting-transcripts) |
| [List Meetings](actions/list-meetings.md) | `GET /meetings` | [docs](https://developer.webex.com/meeting/docs/api/v1/meetings/list-meetings) |
| [List Recordings](actions/list-recordings.md) | `GET /recordings` | [docs](https://developer.webex.com/meeting/docs/api/v1/recordings/list-recordings) |
| [Update a Meeting](actions/update-meeting.md) | `PUT /meetings/:meetingId` | [docs](https://developer.webex.com/docs/api/v1/meetings/update-a-meeting) |
