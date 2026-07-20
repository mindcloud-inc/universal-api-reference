# <img src="https://images.mindcloud.co/apps/icons/b9ff306c-d185-4b4a-9176-fff1a71ae5e6-2_1774962782532.png" alt="HoorayHR logo" width="28" height="28"> HoorayHR: Universal API

Manage personnel files, leave, contracts, time tracking, and teams

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hoorayHR/latest
- **Category:** Human Resources / HRIS
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.hoorayhr.io/
- **Vendor API docs:** https://api.hoorayhr.io/documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Attendance Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Attendance Report](actions/get-attendance-report.md) | GET | Retrieves an attendance report from HoorayHR. |

### Availability

| Action | Method | Description |
| --- | --- | --- |
| [Get Availability](actions/get-availability.md) | GET | Retrieves an availability record from HoorayHR. |
| [List Availabilities](actions/list-availabilities.md) | GET | Retrieves employee availability records from HoorayHR. |

### Contract

| Action | Method | Description |
| --- | --- | --- |
| [Get Contract](actions/get-contract.md) | GET | Retrieves an employment contract from HoorayHR. |

### Contracts

| Action | Method | Description |
| --- | --- | --- |
| [List Contracts](actions/list-contracts.md) | GET | Retrieves employment contract records from HoorayHR. |

### Employment Term

| Action | Method | Description |
| --- | --- | --- |
| [Get Employment Term](actions/get-employment-term.md) | GET | Retrieves an employment term from HoorayHR. |

### Employment Term Assignments

| Action | Method | Description |
| --- | --- | --- |
| [List Employment Term Assignments](actions/list-employment-term-assignments.md) | GET | Retrieves employment term assignments from HoorayHR. |

### Employment Terms

| Action | Method | Description |
| --- | --- | --- |
| [List Employment Terms](actions/list-employment-terms.md) | GET | Retrieves employment term records from HoorayHR. |

### Entities

| Action | Method | Description |
| --- | --- | --- |
| [List Entities](actions/list-entities.md) | GET | Retrieves company entity records from HoorayHR. |

### External Leave Types

| Action | Method | Description |
| --- | --- | --- |
| [List External Leave Types](actions/list-external-leave-types.md) | GET | Retrieves external leave types from HoorayHR. |

### Label

| Action | Method | Description |
| --- | --- | --- |
| [Get Label](actions/get-label.md) | GET | Retrieves a label record from HoorayHR. |

### Labels

| Action | Method | Description |
| --- | --- | --- |
| [List Labels](actions/list-labels.md) | GET | Retrieves label records from the HoorayHR account. |

### Leave Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Leave Type](actions/get-leave-type.md) | GET | Retrieves a leave type from HoorayHR. |

### Leave Types

| Action | Method | Description |
| --- | --- | --- |
| [List Leave Types](actions/list-leave-types.md) | GET | Retrieves leave type records from HoorayHR. |

### Sick Leave Dossiers

| Action | Method | Description |
| --- | --- | --- |
| [List Sick Leave Dossiers](actions/list-sick-leave-dossiers.md) | GET | Retrieves sick leave dossiers from HoorayHR. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [Get Teams Information by User ID](actions/get-teams-information-by-user-id.md) | GET | Retrieves team information for a user from HoorayHR. |
| [List Teams Information](actions/list-teams-information.md) | GET | Retrieves company team information from HoorayHR. |

### Time Off

| Action | Method | Description |
| --- | --- | --- |
| [List Time Off](actions/list-time-off.md) | GET | Retrieves time off records from HoorayHR. |

### Time Zones

| Action | Method | Description |
| --- | --- | --- |
| [List Time Zones](actions/list-time-zones.md) | GET | Retrieves time zone records from HoorayHR. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves an employee record from HoorayHR. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves employee records from the HoorayHR directory. |

### Work Location Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Work Location Categories](actions/list-work-location-categories.md) | GET | Retrieves work location categories from HoorayHR. |

### Working Today

| Action | Method | Description |
| --- | --- | --- |
| [Get Working Today Overview](actions/get-working-today-overview.md) | GET | Retrieves a working today overview from HoorayHR. |

