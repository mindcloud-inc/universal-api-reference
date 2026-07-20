# <img src="https://images.mindcloud.co/apps/icons/orbit-aiforms_1774989608712.png" alt="Orbit AI (Forms) logo" width="28" height="28"> Orbit AI (Forms): Universal API

Create forms, manage submissions, schedule meetings, and run sequences

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/orbitAIForms/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://orbitforms.ai
- **Vendor API docs:** https://docs.orbitforms.ai/developers/api/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Forms](actions/list-forms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orbitAIForms/latest/actions/list-forms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Appointment

| Action | Method | Description |
| --- | --- | --- |
| [Create Meeting](actions/create-meeting.md) | POST |  |

### Availability Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Get Availability Schedule](actions/get-availability-schedule.md) | GET |  |
| [List Availability Schedules](actions/list-availability-schedules.md) | GET |  |

### Calendar Availability

| Action | Method | Description |
| --- | --- | --- |
| [List Available Time Slots](actions/list-available-time-slots.md) | GET |  |

### Event Type

| Action | Method | Description |
| --- | --- | --- |
| [Create Scheduling Page Event Type](actions/create-scheduling-page-event-type.md) | POST |  |
| [Delete Scheduling Page Event Type](actions/delete-scheduling-page-event-type.md) | DELETE |  |
| [Get Scheduling Page Event Type](actions/get-scheduling-page-event-type.md) | GET |  |
| [List Scheduling Page Event Types](actions/list-scheduling-page-event-types.md) | GET |  |
| [Update Scheduling Page Event Type](actions/update-scheduling-page-event-type.md) | PUT |  |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Create Form](actions/create-form.md) | POST |  |
| [Delete Form](actions/delete-form.md) | DELETE |  |
| [Get Form](actions/get-form.md) | GET |  |
| [List Forms](actions/list-forms.md) | GET |  |
| [Update Form](actions/update-form.md) | PUT |  |

### Form Submission

| Action | Method | Description |
| --- | --- | --- |
| [List Form Submissions](actions/list-form-submissions.md) | GET |  |

### Meeting

| Action | Method | Description |
| --- | --- | --- |
| [Get Meeting](actions/get-meeting.md) | GET |  |
| [List Meetings](actions/list-meetings.md) | GET |  |
| [Update Meeting](actions/update-meeting.md) | PUT |  |

### Scheduling Page

| Action | Method | Description |
| --- | --- | --- |
| [Create Scheduling Page](actions/create-scheduling-page.md) | POST |  |
| [Delete Scheduling Page](actions/delete-scheduling-page.md) | DELETE |  |
| [Get Scheduling Page](actions/get-scheduling-page.md) | GET |  |
| [List Scheduling Pages](actions/list-scheduling-pages.md) | GET |  |
| [Update Scheduling Page](actions/update-scheduling-page.md) | PUT |  |

### Sequence

| Action | Method | Description |
| --- | --- | --- |
| [Create Sequence](actions/create-sequence.md) | POST |  |
| [Delete Sequence](actions/delete-sequence.md) | DELETE |  |
| [Get Sequence](actions/get-sequence.md) | GET |  |
| [List Sequences](actions/list-sequences.md) | GET |  |
| [Update Sequence](actions/update-sequence.md) | PUT |  |

### Sequence Enrollment

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact to Sequence](actions/add-contact-to-sequence.md) | POST |  |
| [Remove Contact from Sequence](actions/remove-contact-from-sequence.md) | DELETE |  |

