# <img src="https://images.mindcloud.co/apps/icons/images-16_1774902529669.jpeg" alt="Vyte logo" width="28" height="28"> Vyte: Universal API

Vyte is a scheduling and booking platform API for managing organizations, users, teams, availability, booking pages, events, and related scheduling resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vyte/latest
- **Category:** Productivity / Scheduling
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://vyte.in
- **Vendor API docs:** https://developer.vyte.in/reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vyte/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Appointment

| Action | Method | Description |
| --- | --- | --- |
| [List Team Available Slots](actions/list-team-available-slots.md) | GET | Retrieves available team slots from Vyte. |
| [List Team Slot Days](actions/list-team-slot-days.md) | GET | Retrieves team slot days from Vyte. |

### Availability

| Action | Method | Description |
| --- | --- | --- |
| [Delete User Availabilities](actions/delete-user-availabilities.md) | DELETE | Deletes a user's availabilities from Vyte. |
| [Retrieve User Availabilities](actions/retrieve-user-availabilities.md) | GET | Retrieves a user's availabilities from Vyte. |
| [Set User Availabilities](actions/set-user-availabilities.md) | POST | Sets a user's availabilities in Vyte. |
| [Update User Availabilities](actions/update-user-availabilities.md) | PUT | Updates a user's availabilities in Vyte. |

### Calendar

| Action | Method | Description |
| --- | --- | --- |
| [Delete User Calendar](actions/delete-user-calendar.md) | DELETE | Deletes a user's calendar from Vyte. |
| [List User Calendars](actions/list-user-calendars.md) | GET | Retrieves a user's calendars from Vyte. |
| [Update User Calendars](actions/update-user-calendars.md) | PUT | Updates a user's calendars in Vyte. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Book Event With Team Member](actions/book-event-with-team-member.md) | POST | Books an event with a team member in Vyte. |
| [Cancel Event](actions/cancel-event.md) | PUT | Cancels an event in Vyte. |
| [Confirm Event](actions/confirm-event.md) | PUT | Confirms an event in Vyte. |
| [Create Event](actions/create-event.md) | POST | Creates a new event in Vyte. |
| [List Events](actions/list-events.md) | GET | Retrieves a list of events from Vyte. |
| [List Team Members' Events](actions/list-team-members-events.md) | GET | Retrieves team members' events from Vyte. |
| [Retrieve Event](actions/retrieve-event.md) | GET | Retrieves an event from Vyte. |
| [Update Event](actions/update-event.md) | PUT | Updates an existing event in Vyte. |

### Slot

| Action | Method | Description |
| --- | --- | --- |
| [List Available Slots](actions/list-available-slots.md) | GET | Retrieves available slots from Vyte. |

### Slot Day

| Action | Method | Description |
| --- | --- | --- |
| [List Slot Days](actions/list-slot-days.md) | GET | Retrieves slot days from Vyte. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Create Team](actions/create-team.md) | POST | Creates a new team in Vyte. |
| [Delete Team](actions/delete-team.md) | DELETE | Deletes an existing team from Vyte. |
| [List Teams](actions/list-teams.md) | GET | Retrieves a list of teams from Vyte. |
| [Retrieve Team](actions/retrieve-team.md) | GET | Retrieves a team from Vyte. |
| [Update Team](actions/update-team.md) | PUT | Updates an existing team in Vyte. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in Vyte. |
| [List Users](actions/list-users.md) | GET | Retrieves a list of users from Vyte. |
| [Remove User From Organization](actions/remove-user-from-organization.md) | DELETE | Removes a user from an organization in Vyte. |
| [Retrieve User](actions/retrieve-user.md) | GET | Retrieves a user from Vyte. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Vyte. |

