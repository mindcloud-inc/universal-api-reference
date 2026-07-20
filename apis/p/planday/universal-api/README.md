# <img src="https://images.mindcloud.co/apps/icons/planday_1774905125162.png" alt="Planday logo" width="28" height="28"> Planday: Universal API

Manage staff, schedules, absences, and punch clock data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/planday/latest
- **Category:** Productivity / Scheduling
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.planday.com
- **Vendor API docs:** https://openapi.planday.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Portal Information](actions/get-portal-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planday/latest/actions/get-portal-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Absence Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Absence Request](actions/create-absence-request.md) | POST | Creates a new absence request in Planday. |
| [List Absence Requests](actions/list-absence-requests.md) | GET | Retrieves a list of absence requests from Planday. |

### Absence Type

| Action | Method | Description |
| --- | --- | --- |
| [List Absence Types](actions/list-absence-types.md) | GET | Retrieves a list of absence types from Planday. |

### Department

| Action | Method | Description |
| --- | --- | --- |
| [Create Department](actions/create-department.md) | POST | Creates a new department in Planday. |
| [Get Department](actions/get-department.md) | GET | Retrieves an existing department from Planday. |
| [List Departments](actions/list-departments.md) | GET | Retrieves a list of departments from Planday. |
| [Update Department](actions/update-department.md) | PUT | Updates an existing department in Planday. |

### Employee

| Action | Method | Description |
| --- | --- | --- |
| [Create Employee](actions/create-employee.md) | POST | Creates a new employee in Planday. |
| [Deactivate Employee](actions/deactivate-employee.md) | PUT | Deactivates an existing employee in Planday. |
| [Get Employee](actions/get-employee.md) | GET | Retrieves an existing employee from Planday. |
| [List Deactivated Employees](actions/list-deactivated-employees.md) | GET | Retrieves a list of deactivated employees from Planday. |
| [List Department Employees](actions/list-department-employees.md) | GET | Retrieves employees in a Planday department. |
| [List Employees](actions/list-employees.md) | GET | Retrieves a list of employees from Planday. |
| [Reactivate Employee](actions/reactivate-employee.md) | PUT | Reactivates a deactivated employee in Planday. |
| [Update Employee](actions/update-employee.md) | PUT | Updates an existing employee in Planday. |

### Employee Shift

| Action | Method | Description |
| --- | --- | --- |
| [List Today's Employee Shifts](actions/list-todays-employee-shifts.md) | GET | Retrieves today's employee shifts from Planday. |

### Portal

| Action | Method | Description |
| --- | --- | --- |
| [Get Portal Information](actions/get-portal-information.md) | GET | Retrieves basic portal details from Planday. |

### Position

| Action | Method | Description |
| --- | --- | --- |
| [Create Position](actions/create-position.md) | POST | Creates a new position in Planday. |
| [Get Position](actions/get-position.md) | GET | Retrieves an existing position from Planday. |
| [List Positions](actions/list-positions.md) | GET | Retrieves a list of positions from Planday. |
| [Update Position](actions/update-position.md) | PUT | Updates an existing position in Planday. |

### Punch Clock Shift

| Action | Method | Description |
| --- | --- | --- |
| [List Punch Clock Records](actions/list-punch-clock-records.md) | GET | Retrieves punch clock records from Planday. |

### Shift

| Action | Method | Description |
| --- | --- | --- |
| [Assign Shift](actions/assign-shift.md) | PUT | Assigns an employee to a shift in Planday. |
| [Create Shift](actions/create-shift.md) | POST | Creates a new shift in Planday. |
| [Delete Shift](actions/delete-shift.md) | DELETE | Deletes an existing shift from Planday. |
| [Get Shift](actions/get-shift.md) | GET | Retrieves an existing shift from Planday. |
| [List Shifts](actions/list-shifts.md) | GET | Retrieves a list of shifts from Planday. |
| [Update Shift](actions/update-shift.md) | PUT | Updates an existing shift in Planday. |

### Shift Status

| Action | Method | Description |
| --- | --- | --- |
| [List Shift Statuses](actions/list-shift-statuses.md) | GET | Retrieves a list of shift statuses from Planday. |

### Shift Type

| Action | Method | Description |
| --- | --- | --- |
| [List Shift Types](actions/list-shift-types.md) | GET | Retrieves a list of shift types from Planday. |

