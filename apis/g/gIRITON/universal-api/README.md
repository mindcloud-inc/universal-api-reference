# <img src="https://images.mindcloud.co/apps/icons/g-iriton_1776089663793.png" alt="GIRITON logo" width="28" height="28"> GIRITON: Universal API

Manage attendance, shifts, HR records, and projects

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gIRITON/latest
- **Category:** Human Resources / HRIS
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://giriton.com
- **Vendor API docs:** https://rest.giriton.com/apidoc/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Attendance Activities](actions/list-attendance-activities.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/list-attendance-activities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [List Attendance Activities](actions/list-attendance-activities.md) | GET | Retrieves available attendance activities from GIRITON. |

### Attendance Records

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Attendance Event](actions/create-or-update-attendance-event.md) | PUT | Creates or updates an attendance event in GIRITON. |
| [Delete Attendance Event](actions/delete-attendance-event.md) | DELETE | Deletes an attendance event from GIRITON. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Project Categories](actions/list-project-categories.md) | GET | Retrieves all project categories from GIRITON. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Get Document](actions/get-document.md) | GET | Retrieves a specific document from GIRITON. |
| [Get Document Data](actions/get-document-data.md) | GET | Retrieves data for a specific GIRITON document. |
| [List Documents](actions/list-documents.md) | GET | Retrieves a list of documents from GIRITON. |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Get Person](actions/get-person.md) | GET | Retrieves a specific person from GIRITON. |
| [List Users Employed Between Dates](actions/list-users-employed-between-dates.md) | GET | Retrieves users employed during a selected GIRITON date range. |
| [List Users Employed On Date](actions/list-users-employed-on-date.md) | GET | Retrieves users employed on a selected GIRITON date. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [List Departments](actions/list-departments.md) | GET | Retrieves a list of departments from GIRITON. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Get Agenda](actions/get-agenda.md) | GET | Retrieves a specific agenda from GIRITON. |
| [List Agendas](actions/list-agendas.md) | GET | Retrieves a list of agendas from GIRITON. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects active on a selected GIRITON date. |

### Recordings

| Action | Method | Description |
| --- | --- | --- |
| [Get Agenda Record](actions/get-agenda-record.md) | GET | Retrieves a specific record from a GIRITON agenda. |
| [List Agenda Records](actions/list-agenda-records.md) | GET | Retrieves records from a specific GIRITON agenda. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [List Shifts](actions/list-shifts.md) | GET | Retrieves a list of shifts from GIRITON. |

### Time Off

| Action | Method | Description |
| --- | --- | --- |
| [Add Vacation](actions/add-vacation.md) | POST | Creates a new vacation entry in GIRITON. |

### Time Off Requests

| Action | Method | Description |
| --- | --- | --- |
| [List Attendance Requests](actions/list-attendance-requests.md) | GET | Retrieves a list of attendance requests from GIRITON. |

### Timesheets

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Business Trip](actions/create-or-update-business-trip.md) | PUT | Creates or updates a business trip in GIRITON. |
| [Get Person Attendance Data](actions/get-person-attendance-data.md) | GET | Retrieves configured attendance data for one GIRITON person. |
| [List Attendance Data](actions/list-attendance-data.md) | GET | Retrieves configured attendance data from GIRITON. |
| [List Closed Attendance](actions/list-closed-attendance.md) | GET | Retrieves closed attendance records for a selected GIRITON month. |
| [List Users Activity](actions/list-users-activity.md) | GET | Retrieves user attendance activity for a selected GIRITON day. |

