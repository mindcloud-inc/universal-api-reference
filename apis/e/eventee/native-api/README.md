# Eventee: Native API Reference

A consolidated summary of Eventee's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://publiceventeeapi.docs.apiary.io/
- **API base URL:** `https://api.eventee.com/public/v1`

## Authentication

### API Token

Use an Eventee public API token generated in the Eventee admin under Settings -> Features.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://publiceventeeapi.docs.apiary.io/#reference/authentication)

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Hall](actions/create-hall.md) | `POST /hall` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/halls/create-hall/post) |
| [Create Lecture](actions/create-lecture.md) | `POST /lecture` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/lectures/create-lecture/post) |
| [Create Partner](actions/create-partner.md) | `POST /partner` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/partners/create-partner/post) |
| [Create Pause](actions/create-pause.md) | `POST /pause` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/pauses/create-pause/post) |
| [Create Speaker](actions/create-speaker.md) | `POST /speaker` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/speakers/create-speaker/post) |
| [Create Track](actions/create-track.md) | `POST /label` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/tracks/create-track/post) |
| [Delete Attendee](actions/delete-attendee.md) | `DELETE /attendee` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/participants/remove-attendee/remove) |
| [Delete Hall](actions/delete-hall.md) | `DELETE /hall/{id}` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/halls/update-or-delete-hall/delete) |
| [Delete Lecture](actions/delete-lecture.md) | `DELETE /lecture/{id}` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/lectures/update-or-delete-lecture/delete) |
| [Delete Partner](actions/delete-partner.md) | `DELETE /partner/{id}` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/partners/update-or-delete-partner/delete) |
| [Delete Pause](actions/delete-pause.md) | `DELETE /pause/{id}` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/pauses/update-or-delete-pause/delete) |
| [Delete Registration](actions/delete-registration.md) | `DELETE /registration` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/registrations/remove-registrant/remove) |
| [Delete Speaker](actions/delete-speaker.md) | `DELETE /speaker/{id}` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/speakers/update-or-delete-speaker/delete) |
| [Delete Track](actions/delete-track.md) | `DELETE /label/{id}` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/tracks/update-or-delete-track/delete) |
| [Get Event Content](actions/get-event-content.md) | `GET /content` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/content/get-all-content/get) |
| [Invite Attendees](actions/invite-attendees.md) | `PUT /attendee/invite` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/participants/invite-attendees/invite) |
| [Invite Registrations](actions/invite-registrations.md) | `PUT /registration/invite` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/registrations/invite-registrations/invite) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/groups/get-all/get-all) |
| [List Participants](actions/list-participants.md) | `GET /participants` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/participants/get-all-participants/get-all) |
| [List Partners](actions/list-partners.md) | `GET /partners` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/partners/get-all-partners/get) |
| [List Registrations](actions/list-registrations.md) | `GET /registrations` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/registrations/get-all-registrations/get-all) |
| [List Reviews](actions/list-reviews.md) | `GET /reviews` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/reviews/get-all-reviews/get) |
| [Update Attendee Check-In](actions/update-attendee-check-in.md) | `PUT /attendee/{id}/checkin` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/participants/update-check-in/update-check-in) |
| [Update Hall](actions/update-hall.md) | `PATCH /hall/{id}` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/halls/update-or-delete-hall/update) |
| [Update Lecture](actions/update-lecture.md) | `PATCH /lecture/{id}` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/lectures/update-or-delete-lecture/update) |
| [Update Partner](actions/update-partner.md) | `PATCH /partner/{id}` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/partners/update-or-delete-partner/update) |
| [Update Pause](actions/update-pause.md) | `PATCH /pause/{id}` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/pauses/update-or-delete-pause/update) |
| [Update Speaker](actions/update-speaker.md) | `PATCH /speaker/{id}` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/speakers/update-or-delete-speaker/update) |
| [Update Track](actions/update-track.md) | `PATCH /label/{id}` | [docs](https://publiceventeeapi.docs.apiary.io/#reference/tracks/update-or-delete-track/update) |
