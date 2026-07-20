# HoorayHR: Native API Reference

A consolidated summary of HoorayHR's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://api.hoorayhr.io/documentation/
- **OpenAPI specification:** https://api.hoorayhr.io/swagger.json
- **API base URL:** `https://api.hoorayhr.io`

## Authentication

### Personal API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.hoorayhr.io/swagger.json)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Filtering

Send filters in the query string. Supported operators: `eq`, `gt`, `gte`, `in`, `lt`, `lte`.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Attendance Report](actions/get-attendance-report.md) | `GET /attendance-report` | [docs](https://api.hoorayhr.io/documentation/#/attendance-report/findAttendanceReport) |
| [Get Availability](actions/get-availability.md) | `GET /availability/:id` | [docs](https://api.hoorayhr.io/documentation/#/availability/getAvailability) |
| [Get Contract](actions/get-contract.md) | `GET /contracts/:id` | [docs](https://api.hoorayhr.io/documentation/#/contracts/getContract) |
| [Get Employment Term](actions/get-employment-term.md) | `GET /employment-terms/:id` | [docs](https://api.hoorayhr.io/documentation/#/employment-terms) |
| [Get Label](actions/get-label.md) | `GET /labels/:id` | [docs](https://api.hoorayhr.io/documentation/#/labels/getLabel) |
| [Get Leave Type](actions/get-leave-type.md) | `GET /leave-types/:id` | [docs](https://api.hoorayhr.io/documentation/#/leave-types/getLeaveType) |
| [Get Teams Information by User ID](actions/get-teams-information-by-user-id.md) | `GET /teams-information/:id` | [docs](https://api.hoorayhr.io/documentation/#/teams-information/getTeamsInformation) |
| [Get User](actions/get-user.md) | `GET /users/:id` | [docs](https://api.hoorayhr.io/documentation/#/users/getUser) |
| [Get Working Today Overview](actions/get-working-today-overview.md) | `GET /working-today` | [docs](https://api.hoorayhr.io/documentation/#/working-today/findWorkingToday) |
| [List Availabilities](actions/list-availabilities.md) | `GET /availability` | [docs](https://api.hoorayhr.io/documentation/#/availability/findAvailability) |
| [List Contracts](actions/list-contracts.md) | `GET /contracts` | [docs](https://api.hoorayhr.io/documentation/#/contracts/findContracts) |
| [List Employment Term Assignments](actions/list-employment-term-assignments.md) | `GET /employment-term-assignments` | [docs](https://api.hoorayhr.io/documentation/#/employment-term-assignments) |
| [List Employment Terms](actions/list-employment-terms.md) | `GET /employment-terms` | [docs](https://api.hoorayhr.io/documentation/#/employment-terms) |
| [List Entities](actions/list-entities.md) | `GET /entities` | [docs](https://api.hoorayhr.io/documentation/#/entities/findEntities) |
| [List External Leave Types](actions/list-external-leave-types.md) | `GET /external-leave-types` | [docs](https://api.hoorayhr.io/documentation/#/external-leave-types/findExternalLeaveTypes) |
| [List Labels](actions/list-labels.md) | `GET /labels` | [docs](https://api.hoorayhr.io/documentation/#/labels/findLabels) |
| [List Leave Types](actions/list-leave-types.md) | `GET /leave-types` | [docs](https://api.hoorayhr.io/documentation/#/leave-types/findLeaveTypes) |
| [List Sick Leave Dossiers](actions/list-sick-leave-dossiers.md) | `GET /sick-leave-dossiers` | [docs](https://api.hoorayhr.io/documentation/#/sick-leave-dossiers/findSickLeaveDossiers) |
| [List Teams Information](actions/list-teams-information.md) | `GET /teams-information` | [docs](https://api.hoorayhr.io/documentation/#/teams-information/findTeamsInformation) |
| [List Time Off](actions/list-time-off.md) | `GET /time-off` | [docs](https://api.hoorayhr.io/documentation/#/time-off/findTimeOff) |
| [List Time Zones](actions/list-time-zones.md) | `GET /time-zones` | [docs](https://api.hoorayhr.io/documentation/#/time-zones/findTimeZones) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://api.hoorayhr.io/documentation/#/users/findUsers) |
| [List Work Location Categories](actions/list-work-location-categories.md) | `GET /work-location-categories` | [docs](https://api.hoorayhr.io/documentation/#/work-location-categories/findWorkLocationCategories) |
