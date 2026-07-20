# GIRITON: Native API Reference

A consolidated summary of GIRITON's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://rest.giriton.com/apidoc/
- **OpenAPI specification:** https://rest.giriton.com/system/api/swagger.json
- **API base URL:** `https://rest.giriton.com/system/api`

## Authentication

### API Key

Use a GIRITON REST API token from Paired devices. The token is sent in the giriton-token request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
giriton-token: <apiKey>
```

[Official authentication documentation](https://rest.giriton.com/apidoc/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 200; accepted range 1–200). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Vacation](actions/add-vacation.md) | `POST /attendance/vacation` | [docs](https://rest.giriton.com/apidoc/#/Attendance/addVacation) |
| [Create Or Update Attendance Event](actions/create-or-update-attendance-event.md) | `POST /attendance/attendanceEvent` | [docs](https://rest.giriton.com/apidoc/#/Attendance/addAttendanceEventJsonBody) |
| [Create Or Update Business Trip](actions/create-or-update-business-trip.md) | `POST /attendance/businessTrip` | [docs](https://rest.giriton.com/apidoc/#/Attendance/addUpdateBusinessTrip) |
| [Delete Attendance Event](actions/delete-attendance-event.md) | `DELETE /attendance/attendanceEvent` | [docs](https://rest.giriton.com/apidoc/#/Attendance/removeAttendanceEvent) |
| [Get Agenda](actions/get-agenda.md) | `GET /agendas/:agendaId` | [docs](https://rest.giriton.com/apidoc/#/Agenda/getCatalog) |
| [Get Agenda Record](actions/get-agenda-record.md) | `GET /agendas/:agendaId/records/:recordId` | [docs](https://rest.giriton.com/apidoc/#/Agenda/getRecord) |
| [Get Document](actions/get-document.md) | `GET /documents/:documentId` | [docs](https://rest.giriton.com/apidoc/#/Documents/getDocument) |
| [Get Document Data](actions/get-document-data.md) | `GET /documents/:documentId/data` | [docs](https://rest.giriton.com/apidoc/#/Documents/getDocumentData) |
| [Get Person](actions/get-person.md) | `GET /hr/person/:id` | [docs](https://rest.giriton.com/apidoc/#/Human%20Resources/getPerson) |
| [Get Person Attendance Data](actions/get-person-attendance-data.md) | `GET /attendance/personAttendanceData` | [docs](https://rest.giriton.com/apidoc/#/Attendance/getPersonAttendanceData) |
| [List Agenda Records](actions/list-agenda-records.md) | `GET /agendas/:agendaId/records` | [docs](https://rest.giriton.com/apidoc/#/Agenda/getRecords) |
| [List Agendas](actions/list-agendas.md) | `GET /agendas` | [docs](https://rest.giriton.com/apidoc/#/Agenda/getCatalogs) |
| [List Attendance Activities](actions/list-attendance-activities.md) | `GET /attendance/attendanceActivities` | [docs](https://rest.giriton.com/apidoc/#/Attendance/getAttendanceActivities) |
| [List Attendance Data](actions/list-attendance-data.md) | `GET /attendance/attendanceData` | [docs](https://rest.giriton.com/apidoc/#/Attendance/getAttendanceData) |
| [List Attendance Requests](actions/list-attendance-requests.md) | `GET /requests/requests` | [docs](https://rest.giriton.com/apidoc/#/Attendance%20requests/getAttendanceRequests) |
| [List Closed Attendance](actions/list-closed-attendance.md) | `GET /attendance/closedAttendance` | [docs](https://rest.giriton.com/apidoc/#/Attendance/getClosedAttendance) |
| [List Departments](actions/list-departments.md) | `GET /hr/departments` | [docs](https://rest.giriton.com/apidoc/#/Human%20Resources/getDepartments) |
| [List Documents](actions/list-documents.md) | `GET /documents` | [docs](https://rest.giriton.com/apidoc/#/Documents/getDocuments) |
| [List Project Categories](actions/list-project-categories.md) | `GET /projects/categories` | [docs](https://rest.giriton.com/apidoc/#/Projects/getCategories) |
| [List Projects](actions/list-projects.md) | `GET /projects/projects` | [docs](https://rest.giriton.com/apidoc/#/Projects/getProjects) |
| [List Shifts](actions/list-shifts.md) | `GET /shift/shifts` | [docs](https://rest.giriton.com/apidoc/#/Shift/getShifts) |
| [List Users Activity](actions/list-users-activity.md) | `GET /attendance/usersActivity` | [docs](https://rest.giriton.com/apidoc/#/Attendance/getUsersActivity) |
| [List Users Employed Between Dates](actions/list-users-employed-between-dates.md) | `GET /hr/usersEmployedBetween` | [docs](https://rest.giriton.com/apidoc/#/Human%20Resources/getUsersEmployedBetween) |
| [List Users Employed On Date](actions/list-users-employed-on-date.md) | `GET /hr/usersEmployedOn` | [docs](https://rest.giriton.com/apidoc/#/Human%20Resources/getUsersEmployedOn) |
