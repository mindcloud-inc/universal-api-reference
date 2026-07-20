# eTermin: Native API Reference

A consolidated summary of eTermin's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://www.etermin.net/online-terminplaner-api
- **OpenAPI specification:** https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0
- **API base URL:** `https://www.etermin.net`

## Authentication

### API Key + Signature

### Credentials

- **API Key:** `apiKey` · required
- **Private Key:** `privateKey` · required · The eTermin secret key used to generate the request signature for every API call.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.etermin.net/online-terminplaner-api)

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Calendar Services](actions/assign-calendar-services.md) | `POST /api/calendarservice` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/CalendarService/post_api_calendarservice) |
| [Create Appointment](actions/create-appointment.md) | `POST /api/appointment` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Appointment/post_api_appointment) |
| [Create Calendar](actions/create-calendar.md) | `POST /api/calendar` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Calendar/post_api_calendar) |
| [Create Calendar Absence](actions/create-calendar-absence.md) | `POST /api/calendarsnonworkingtimes` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/CalendarsNonWorkingTimes/post_api_calendarsnonworkingtimes) |
| [Create Contact](actions/create-contact.md) | `POST /api/contact` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Contact/post_api_contact) |
| [Create Service](actions/create-service.md) | `POST /api/service` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Service/post_api_service) |
| [Create Service Group](actions/create-service-group.md) | `POST /api/servicegroup` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Servicegroup/post_api_servicegroup) |
| [Create Working Times](actions/create-working-times.md) | `POST /api/workingtimes` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/WorkingTimes/post_api_workingtimes) |
| [Create Working Times by Date](actions/create-working-times-by-date.md) | `POST /api/workingtimesdate` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/WorkingTimesDate/post_api_workingtimesdate) |
| [Delete Appointment](actions/delete-appointment.md) | `DELETE /api/appointment` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Appointment/delete_api_appointment) |
| [Delete Calendar](actions/delete-calendar.md) | `DELETE /api/calendar` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Calendar/delete_api_calendar) |
| [Delete Calendar Absence](actions/delete-calendar-absence.md) | `DELETE /api/calendarsnonworkingtimes` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/CalendarsNonWorkingTimes/delete_api_calendarsnonworkingtimes) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /api/contact` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Contact/delete_api_contact) |
| [Delete Service](actions/delete-service.md) | `DELETE /api/service` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Service/delete_api_service) |
| [Delete Service Group](actions/delete-service-group.md) | `DELETE /api/servicegroup` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Servicegroup/delete_api_servicegroup) |
| [Delete Working Times](actions/delete-working-times.md) | `DELETE /api/workingtimes` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/WorkingTimes/delete_api_workingtimes) |
| [Delete Working Times by Date](actions/delete-working-times-by-date.md) | `DELETE /api/workingtimesdate` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/WorkingTimesDate/delete_api_workingtimesdate) |
| [List Appointments](actions/list-appointments.md) | `GET /api/appointment` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Appointment/get_api_appointment) |
| [List Available Time Slots](actions/list-available-time-slots.md) | `GET /api/timeslots` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Timeslots/get_api_timeslots) |
| [List Calendar Absences](actions/list-calendar-absences.md) | `GET /api/calendarsnonworkingtimes` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/CalendarsNonWorkingTimes/get_api_calendarsnonworkingtimes) |
| [List Calendar Return Times](actions/list-calendar-return-times.md) | `GET /api/calendarreturntime` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/CalendarReturnTime/get_api_calendarreturntime) |
| [List Calendar Services](actions/list-calendar-services.md) | `GET /api/calendarservice` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/CalendarService/get_api_calendarservice) |
| [List Calendars](actions/list-calendars.md) | `GET /api/calendar` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Calendar/get_api_calendar) |
| [List Contacts](actions/list-contacts.md) | `GET /api/contact` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Contact/get_api_contact) |
| [List Deleted Appointments](actions/list-deleted-appointments.md) | `GET /api/appointmentdeleted` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/AppointmentDeleted/get_api_appointmentdeleted) |
| [List Service Calendars](actions/list-service-calendars.md) | `GET /api/servicecalendar` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Servicecalendar/get_api_servicecalendar) |
| [List Service Groups](actions/list-service-groups.md) | `GET /api/servicegroup` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Servicegroup/get_api_servicegroup) |
| [List Services](actions/list-services.md) | `GET /api/service` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Service/get_api_service) |
| [List Working Times](actions/list-working-times.md) | `GET /api/workingtimes` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/WorkingTimes/get_api_workingtimes) |
| [List Working Times by Date](actions/list-working-times-by-date.md) | `GET /api/workingtimesdate` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/WorkingTimesDate/get_api_workingtimesdate) |
| [Sync Appointments](actions/sync-appointments.md) | `GET /api/appointmentsync` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/AppointmentSync/get_api_appointmentsync) |
| [Unassign Calendar Services](actions/unassign-calendar-services.md) | `DELETE /api/calendarservice` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/CalendarService/delete_api_calendarservice) |
| [Update Appointment](actions/update-appointment.md) | `PUT /api/appointment` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Appointment/put_api_appointment) |
| [Update Calendar](actions/update-calendar.md) | `PUT /api/calendar` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Calendar/put_api_calendar) |
| [Update Calendar Absence](actions/update-calendar-absence.md) | `PUT /api/calendarsnonworkingtimes` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/CalendarsNonWorkingTimes/put_api_calendarsnonworkingtimes) |
| [Update Contact](actions/update-contact.md) | `PUT /api/contact` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Contact/put_api_contact) |
| [Update Service](actions/update-service.md) | `PUT /api/service` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Service/put_api_service) |
| [Update Service Group](actions/update-service-group.md) | `PUT /api/servicegroup` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Servicegroup/put_api_servicegroup) |
| [Update Working Times](actions/update-working-times.md) | `PUT /api/workingtimes` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/WorkingTimes/put_api_workingtimes) |
| [Update Working Times by Date](actions/update-working-times-by-date.md) | `PUT /api/workingtimesdate` | [docs](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/WorkingTimesDate/put_api_workingtimesdate) |
