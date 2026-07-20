# <img src="https://images.mindcloud.co/apps/icons/images-9_1775853775356.jpeg" alt="Cisco Webex Meetings logo" width="28" height="28"> Cisco Webex Meetings: Universal API

Schedule, manage, and review Webex meetings and recordings

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ciscoWebexMeetings/latest
- **Category:** Communication / Video Communications
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://developer.webex.com/meeting/docs/getting-started
- **Vendor API docs:** https://developer.webex.com/meeting/docs/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Meetings](actions/list-meetings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/list-meetings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Meeting

| Action | Method | Description |
| --- | --- | --- |
| [Create a Meeting](actions/create-meeting.md) | POST | Creates a new meeting in Cisco Webex Meetings. |
| [Delete a Meeting](actions/delete-meeting.md) | DELETE | Deletes an existing meeting from Cisco Webex Meetings. |
| [Delete a Summary](actions/delete-summary.md) | DELETE | Deletes an existing meeting summary from Cisco Webex Meetings. |
| [Download a Meeting Transcript](actions/download-meeting-transcript.md) | GET | Retrieves a downloadable meeting transcript from Cisco Webex Meetings. |
| [Get a Meeting](actions/get-meeting.md) | GET | Retrieves a meeting from Cisco Webex Meetings. |
| [List Meeting Transcripts](actions/list-meeting-transcripts.md) | GET | Retrieves meeting transcripts from Cisco Webex Meetings. |
| [List Meetings](actions/list-meetings.md) | GET | Retrieves meetings from Cisco Webex Meetings. |
| [Update a Meeting](actions/update-meeting.md) | PUT | Updates an existing meeting in Cisco Webex Meetings. |

### Recording

| Action | Method | Description |
| --- | --- | --- |
| [Delete a Recording](actions/delete-recording.md) | DELETE | Deletes an existing recording from Cisco Webex Meetings. |
| [Get Recording Details](actions/get-recording-details.md) | GET | Retrieves recording details from Cisco Webex Meetings. |
| [List Recordings](actions/list-recordings.md) | GET | Retrieves recordings from Cisco Webex Meetings. |

