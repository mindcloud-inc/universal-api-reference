# <img src="https://images.mindcloud.co/apps/icons/e-termin_1773953277846.png" alt="eTermin logo" width="28" height="28"> eTermin: Universal API

eTermin is an online appointment scheduling platform with a REST API for calendars, appointments, contacts, services, availability, and schedule management.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eTermin/latest
- **Category:** Productivity / Scheduling
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.etermin.net
- **Vendor API docs:** https://www.etermin.net/online-terminplaner-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Calendars](actions/list-calendars.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-calendars?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Appointment

| Action | Method | Description |
| --- | --- | --- |
| [Create Appointment](actions/create-appointment.md) | POST | Creates a new appointment in eTermin. |
| [Delete Appointment](actions/delete-appointment.md) | DELETE | Deletes an existing appointment from eTermin. |
| [List Appointments](actions/list-appointments.md) | GET | Retrieves appointments from eTermin. |
| [List Deleted Appointments](actions/list-deleted-appointments.md) | GET | Retrieves deleted appointments from eTermin. |
| [Sync Appointments](actions/sync-appointments.md) | GET | Retrieves appointment changes from eTermin using a sync token. |
| [Update Appointment](actions/update-appointment.md) | PUT | Updates an existing appointment in eTermin. |

### Calendar

| Action | Method | Description |
| --- | --- | --- |
| [Create Calendar](actions/create-calendar.md) | POST | Creates a new calendar in eTermin. |
| [Delete Calendar](actions/delete-calendar.md) | DELETE | Deletes an existing calendar from eTermin. |
| [List Calendars](actions/list-calendars.md) | GET | Retrieves calendars from eTermin. |
| [Update Calendar](actions/update-calendar.md) | PUT | Updates an existing calendar in eTermin. |

### Calendar Absence

| Action | Method | Description |
| --- | --- | --- |
| [Create Calendar Absence](actions/create-calendar-absence.md) | POST | Creates a new calendar absence in eTermin. |
| [Delete Calendar Absence](actions/delete-calendar-absence.md) | DELETE | Deletes an existing calendar absence from eTermin. |
| [List Calendar Absences](actions/list-calendar-absences.md) | GET | Retrieves calendar absences from eTermin. |
| [Update Calendar Absence](actions/update-calendar-absence.md) | PUT | Updates an existing calendar absence in eTermin. |

### Calendar Return Time

| Action | Method | Description |
| --- | --- | --- |
| [List Calendar Return Times](actions/list-calendar-return-times.md) | GET | Retrieves calendar return times from eTermin. |

### Calendar Service

| Action | Method | Description |
| --- | --- | --- |
| [Assign Calendar Services](actions/assign-calendar-services.md) | POST | Assigns services to a calendar in eTermin. |
| [List Calendar Services](actions/list-calendar-services.md) | GET | Retrieves services assigned to a calendar in eTermin. |
| [Unassign Calendar Services](actions/unassign-calendar-services.md) | DELETE | Removes services from a calendar in eTermin. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in eTermin. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from eTermin. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from eTermin. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in eTermin. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [Create Service](actions/create-service.md) | POST | Creates a new service in eTermin. |
| [Delete Service](actions/delete-service.md) | DELETE | Deletes an existing service from eTermin. |
| [List Services](actions/list-services.md) | GET | Retrieves services from eTermin. |
| [Update Service](actions/update-service.md) | PUT | Updates an existing service in eTermin. |

### Service Calendar

| Action | Method | Description |
| --- | --- | --- |
| [List Service Calendars](actions/list-service-calendars.md) | GET | Retrieves calendars assigned to a service in eTermin. |

### Service Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Service Group](actions/create-service-group.md) | POST | Creates a new service group in eTermin. |
| [Delete Service Group](actions/delete-service-group.md) | DELETE | Deletes an existing service group from eTermin. |
| [List Service Groups](actions/list-service-groups.md) | GET | Retrieves service groups from eTermin. |
| [Update Service Group](actions/update-service-group.md) | PUT | Updates an existing service group in eTermin. |

### Time Slot

| Action | Method | Description |
| --- | --- | --- |
| [List Available Time Slots](actions/list-available-time-slots.md) | GET | Retrieves available time slots from eTermin. |

### Working Time

| Action | Method | Description |
| --- | --- | --- |
| [Create Working Times](actions/create-working-times.md) | POST | Creates new working times in eTermin. |
| [Delete Working Times](actions/delete-working-times.md) | DELETE | Deletes existing working times from eTermin. |
| [List Working Times](actions/list-working-times.md) | GET | Retrieves working times from eTermin. |
| [Update Working Times](actions/update-working-times.md) | PUT | Updates existing working times in eTermin. |

### Working Time Date

| Action | Method | Description |
| --- | --- | --- |
| [Create Working Times by Date](actions/create-working-times-by-date.md) | POST | Creates working times by date in eTermin. |
| [Delete Working Times by Date](actions/delete-working-times-by-date.md) | DELETE | Deletes working times by date from eTermin. |
| [List Working Times by Date](actions/list-working-times-by-date.md) | GET | Retrieves working times by date from eTermin. |
| [Update Working Times by Date](actions/update-working-times-by-date.md) | PUT | Updates working times by date in eTermin. |

