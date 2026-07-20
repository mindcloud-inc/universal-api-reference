# <img src="https://images.mindcloud.co/apps/icons/image-2841_1777479669072.png" alt="Airmeet logo" width="28" height="28"> Airmeet: Universal API

Create, manage, and analyze Airmeet events and registrations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/airmeet/latest
- **Category:** Marketing / Events & Webinars
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.airmeet.com
- **Vendor API docs:** https://help.airmeet.com/support/solutions/articles/82000467794-airmeet-public-api-introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Airmeets](actions/list-airmeets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/list-airmeets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Obtain Access Token](actions/obtain-access-token.md) | POST | Creates a new access token in Airmeet. |

### Attendance Records

| Action | Method | Description |
| --- | --- | --- |
| [List Booth Attendees](actions/list-booth-attendees.md) | GET | Finds booth attendance records in Airmeet. |
| [List Event Replay Attendees](actions/list-event-replay-attendees.md) | GET | Finds event replay attendees in Airmeet. |

### Attendees

| Action | Method | Description |
| --- | --- | --- |
| [Add Authorized Attendee](actions/add-authorized-attendee.md) | POST | Creates an authorized attendee in Airmeet. |
| [Block Attendee](actions/block-attendee.md) | PUT | Blocks attendee access in a specific Airmeet. |
| [List Event Attendees](actions/list-event-attendees.md) | GET | Finds event attendance records in Airmeet. |
| [List Participants](actions/list-participants.md) | GET | Finds participants in a specific Airmeet event. |
| [List Session Attendees](actions/list-session-attendees.md) | GET | Finds session attendance records in Airmeet. |
| [Unblock Attendee](actions/unblock-attendee.md) | PUT | Restores attendee access in a specific Airmeet. |

### Attribution Events

| Action | Method | Description |
| --- | --- | --- |
| [List Registration UTMs](actions/list-registration-ut-ms.md) | GET | Finds registration UTM data in Airmeet. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Registration Fields](actions/list-custom-registration-fields.md) | GET | Finds custom registration fields in an Airmeet. |

### Custom Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Booth](actions/create-booth.md) | POST | Creates a new booth in Airmeet. |
| [List Booths](actions/list-booths.md) | GET | Finds booths in a specific Airmeet event. |
| [List Event Tracks](actions/list-event-tracks.md) | GET | Finds event tracks in a specific Airmeet. |
| [List Poll Responses](actions/list-poll-responses.md) | GET | Finds poll responses in a specific Airmeet. |
| [List Questions Asked](actions/list-questions-asked.md) | GET | Finds questions asked in a specific Airmeet. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Create Airmeet](actions/create-airmeet.md) | POST | Creates a new event in Airmeet. |
| [Duplicate Event](actions/duplicate-event.md) | POST | Creates a duplicate event in Airmeet. |
| [List Airmeets](actions/list-airmeets.md) | GET | Finds Airmeet events accessible to your token. |
| [List Events in Series](actions/list-events-in-series.md) | GET | Finds events in an Airmeet event series. |
| [Update Airmeet Status](actions/update-airmeet-status.md) | PUT | Updates the status of an Airmeet event. |

### Landing Pages

| Action | Method | Description |
| --- | --- | --- |
| [Customize Event Landing Page](actions/customize-event-landing-page.md) | PUT | Updates an event landing page in Airmeet. |

### Programs

| Action | Method | Description |
| --- | --- | --- |
| [List Event Series](actions/list-event-series.md) | GET | Finds event series in an Airmeet community. |

### Recordings

| Action | Method | Description |
| --- | --- | --- |
| [List Session Recordings](actions/list-session-recordings.md) | GET | Finds session recording links in Airmeet. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Create Session](actions/create-session.md) | POST | Creates a new session in Airmeet. |
| [Delete Session](actions/delete-session.md) | DELETE | Deletes an existing session from Airmeet. |
| [List Sessions](actions/list-sessions.md) | GET | Finds sessions in a specific Airmeet event. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Add Speaker](actions/add-speaker.md) | POST | Creates a new speaker in Airmeet. |

