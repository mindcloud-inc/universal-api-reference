# <img src="https://images.mindcloud.co/apps/icons/shifts_1776088899372.png" alt="7shifts logo" width="28" height="28"> 7shifts: Universal API

Restaurant workforce platform for scheduling, time punches, labor, user, role, department, and location data through the 7shifts API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/shifts/latest
- **Category:** Productivity / Scheduling
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.7shifts.com
- **Vendor API docs:** https://developers.7shifts.com/docs/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Contacts](actions/get-user-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shifts/latest/actions/get-user-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Assignment

| Action | Method | Description |
| --- | --- | --- |
| [List Assignments](actions/list-assignments.md) | GET | Lists a user's assignments in 7shifts. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [List Companies](actions/list-companies.md) | GET | Lists the company records in 7shifts. |
| [Retrieve Company](actions/retrieve-company.md) | GET | Retrieves a company record from 7shifts. |
| [Retrieve Labor Settings](actions/retrieve-labor-settings.md) | GET | Retrieves company labor settings from 7shifts. |

### Compensations

| Action | Method | Description |
| --- | --- | --- |
| [Create User Wage](actions/create-user-wage.md) | POST | Creates a new user wage in 7shifts. |
| [List User Wages](actions/list-user-wages.md) | GET | Lists a user's wages in 7shifts. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Get User Contacts](actions/get-user-contacts.md) | GET | Lists the user contacts in 7shifts. |
| [Retrieve User Contact](actions/retrieve-user-contact.md) | GET | Retrieves a user contact from 7shifts. |

### Departments

| Action | Method | Description |
| --- | --- | --- |
| [Create Department](actions/create-department.md) | POST | Creates a new department in 7shifts. |
| [List Departments](actions/list-departments.md) | GET | Lists the department records in 7shifts. |
| [Retrieve Department](actions/retrieve-department.md) | GET | Retrieves current department details from 7shifts. |
| [Update Department](actions/update-department.md) | PUT | Updates an existing department in 7shifts. |

### Employment Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Employment Record](actions/create-employment-record.md) | POST | Creates a new employment record in 7shifts. |
| [List Employment Records](actions/list-employment-records.md) | GET | Lists the employment records in 7shifts. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Create Location](actions/create-location.md) | POST | Creates a new location in 7shifts. |
| [List Locations](actions/list-locations.md) | GET | Lists the location records in 7shifts. |
| [List Users Authorized Locations](actions/list-users-authorized-locations.md) | GET | Lists a user's authorized locations in 7shifts. |
| [Retrieve Location](actions/retrieve-location.md) | GET | Retrieves current location details from 7shifts. |
| [Update Location](actions/update-location.md) | PUT | Updates an existing location in 7shifts. |

### Role Assignment

| Action | Method | Description |
| --- | --- | --- |
| [Create Role Assignment](actions/create-role-assignment.md) | POST | Creates a role assignment in 7shifts. |
| [List Role Assignments](actions/list-role-assignments.md) | GET | Lists a user's role assignments in 7shifts. |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [Create Role](actions/create-role.md) | POST | Creates a new role in 7shifts. |
| [List Roles](actions/list-roles.md) | GET | Lists the role records in 7shifts. |
| [Retrieve Role](actions/retrieve-role.md) | GET | Retrieves current role details from 7shifts. |
| [Update Role](actions/update-role.md) | PUT | Updates an existing role in 7shifts. |

### Shift

| Action | Method | Description |
| --- | --- | --- |
| [Create Shift](actions/create-shift.md) | POST | Creates a new shift in 7shifts. |
| [Delete Shift](actions/delete-shift.md) | DELETE | Deletes an existing shift from 7shifts. |
| [List Shifts](actions/list-shifts.md) | GET | Lists the shift records in 7shifts. |
| [Retrieve Shift](actions/retrieve-shift.md) | GET | Retrieves current shift details from 7shifts. |
| [Update Shift](actions/update-shift.md) | PUT | Updates an existing shift in 7shifts. |

### Time Punch

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Punch](actions/create-time-punch.md) | POST | Creates a new time punch in 7shifts. |
| [List Time Punches](actions/list-time-punches.md) | GET | Lists the time punches in 7shifts. |
| [Retrieve Time Punch](actions/retrieve-time-punch.md) | GET | Retrieves a time punch from 7shifts. |
| [Update Time Punch](actions/update-time-punch.md) | PUT | Updates an existing time punch in 7shifts. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in 7shifts. |
| [Deactivate User](actions/deactivate-user.md) | DELETE | Deactivates an existing user in 7shifts. |
| [List Users](actions/list-users.md) | GET | Lists the user records in 7shifts. |
| [Retrieve Identity](actions/retrieve-identity.md) | GET | Retrieves current identity details from 7shifts. |
| [Retrieve User](actions/retrieve-user.md) | GET | Retrieves current user details from 7shifts. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in 7shifts. |

