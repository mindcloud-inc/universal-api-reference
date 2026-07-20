# <img src="https://images.mindcloud.co/apps/icons/follow-up-boss_1773333786447.png" alt="Follow Up Boss logo" width="28" height="28"> Follow Up Boss: Universal API

Manage real estate leads, tasks, appointments, and communication

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/followUpBossV2/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.followupboss.com
- **Vendor API docs:** https://docs.followupboss.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates a new event in Follow Up Boss. |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from Follow Up Boss. |

### Appointments

| Action | Method | Description |
| --- | --- | --- |
| [Create Appointment](actions/create-appointment.md) | POST | Creates a new appointment in Follow Up Boss. |
| [Get Appointment](actions/get-appointment.md) | GET | Retrieves an appointment from Follow Up Boss. |
| [List Appointments](actions/list-appointments.md) | GET | Retrieves appointments from Follow Up Boss. |
| [Update Appointment](actions/update-appointment.md) | PUT | Updates an existing appointment in Follow Up Boss. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Check Duplicate Person](actions/check-duplicate-person.md) | GET | Finds duplicate people in Follow Up Boss by email or phone. |
| [Create Person](actions/create-person.md) | POST | Creates a new person in Follow Up Boss. |
| [Get Person](actions/get-person.md) | GET | Retrieves a person from Follow Up Boss. |
| [List Events](actions/list-events.md) | GET | Retrieves events from Follow Up Boss. |
| [List People](actions/list-people.md) | GET | Retrieves people from Follow Up Boss. |
| [List Unclaimed People](actions/list-unclaimed-people.md) | GET | Retrieves unclaimed people from Follow Up Boss. |
| [Update Person](actions/update-person.md) | PUT | Updates an existing person in Follow Up Boss. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves custom fields from Follow Up Boss. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST | Creates a new note in Follow Up Boss. |
| [Get Note](actions/get-note.md) | GET | Retrieves a note from Follow Up Boss. |
| [Update Note](actions/update-note.md) | PUT | Updates an existing note in Follow Up Boss. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Follow Up Boss. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Follow Up Boss. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from Follow Up Boss. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Follow Up Boss. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Follow Up Boss. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Follow Up Boss. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Follow Up Boss. |

