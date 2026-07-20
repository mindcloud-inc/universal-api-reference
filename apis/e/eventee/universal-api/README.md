# <img src="https://images.mindcloud.co/apps/icons/eventee_1775839593918.png" alt="Eventee logo" width="28" height="28"> Eventee: Universal API

Manage Eventee event content, attendees, registrations, reviews, halls, lectures, partners, pauses, speakers, and tracks through the Eventee Public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eventee/latest
- **Category:** Marketing / Events & Webinars
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://eventee.com
- **Vendor API docs:** https://publiceventeeapi.docs.apiary.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Event Content](actions/get-event-content.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventee/latest/actions/get-event-content?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Attendees

| Action | Method | Description |
| --- | --- | --- |
| [Delete Attendee](actions/delete-attendee.md) | DELETE | Deletes an attendee from Eventee. |
| [Invite Attendees](actions/invite-attendees.md) | POST | Creates attendee invitations in Eventee. |
| [List Participants](actions/list-participants.md) | GET | Retrieves participants from Eventee. |
| [Update Attendee Check-In](actions/update-attendee-check-in.md) | PUT | Updates attendee check-in status in Eventee. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Create Partner](actions/create-partner.md) | POST | Creates a partner in Eventee. |
| [Delete Partner](actions/delete-partner.md) | DELETE | Deletes an existing partner from Eventee. |
| [List Partners](actions/list-partners.md) | GET | Retrieves partners from Eventee. |
| [Update Partner](actions/update-partner.md) | PUT | Updates an existing partner in Eventee. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Speaker](actions/create-speaker.md) | POST | Creates a speaker in Eventee. |
| [Delete Speaker](actions/delete-speaker.md) | DELETE | Deletes an existing speaker from Eventee. |
| [Update Speaker](actions/update-speaker.md) | PUT | Updates an existing speaker in Eventee. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Content](actions/get-event-content.md) | GET | Retrieves event content from Eventee. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from Eventee. |

### Invitations

| Action | Method | Description |
| --- | --- | --- |
| [Delete Registration](actions/delete-registration.md) | DELETE | Deletes a registration from Eventee. |
| [Invite Registrations](actions/invite-registrations.md) | POST | Creates registration invitations in Eventee. |
| [List Registrations](actions/list-registrations.md) | GET | Retrieves registrations from Eventee. |

### Labels

| Action | Method | Description |
| --- | --- | --- |
| [Create Track](actions/create-track.md) | POST | Creates a track in Eventee. |
| [Delete Track](actions/delete-track.md) | DELETE | Deletes an existing track from Eventee. |
| [Update Track](actions/update-track.md) | PUT | Updates an existing track in Eventee. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Create Hall](actions/create-hall.md) | POST | Creates a hall in Eventee. |
| [Delete Hall](actions/delete-hall.md) | DELETE | Deletes an existing hall from Eventee. |
| [Update Hall](actions/update-hall.md) | PUT | Updates an existing hall in Eventee. |

### Satisfaction Responses

| Action | Method | Description |
| --- | --- | --- |
| [List Reviews](actions/list-reviews.md) | GET | Retrieves reviews from Eventee. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Create Lecture](actions/create-lecture.md) | POST | Creates a lecture in Eventee. |
| [Create Pause](actions/create-pause.md) | POST | Creates a pause in Eventee. |
| [Delete Lecture](actions/delete-lecture.md) | DELETE | Deletes an existing lecture from Eventee. |
| [Delete Pause](actions/delete-pause.md) | DELETE | Deletes an existing pause from Eventee. |
| [Update Lecture](actions/update-lecture.md) | PUT | Updates an existing lecture in Eventee. |
| [Update Pause](actions/update-pause.md) | PUT | Updates an existing pause in Eventee. |

