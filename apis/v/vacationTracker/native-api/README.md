# Vacation Tracker: Native API Reference

A consolidated summary of Vacation Tracker's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://vacationtracker.io/developers/api
- **API base URL:** `https://api.vacationtracker.io/v1`

## Authentication

### API Key

Authenticate requests with a Vacation Tracker API key sent in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required · Vacation Tracker API key used in the x-api-key request header.

[Official authentication documentation](https://vacationtracker.io/developers/api)

## API conventions

Response data is read from `data`. The next-page cursor is read from `nextToken`.

## Pagination

Use `limit` in the query string to set the page size (default 300; accepted range 25–500). Use `nextToken` in the query string as the pagination cursor; numbering starts at 0.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Departments](actions/list-departments.md) | `GET /departments` | [docs](https://vacationtracker.io/developers/api/departments/listDepartments) |
| [List Labels](actions/list-labels.md) | `GET /labels` | [docs](https://vacationtracker.io/developers/api/labels/listLabels) |
| [List Leave Types](actions/list-leave-types.md) | `GET /leave-types` | [docs](https://vacationtracker.io/developers/api/leavetypes/listLeaveTypes) |
| [List Leaves](actions/list-leaves.md) | `GET /leaves` | [docs](https://vacationtracker.io/developers/api/leaves/listLeaves) |
| [List Locations](actions/list-locations.md) | `GET /locations` | [docs](https://vacationtracker.io/developers/api/locations/listLocations) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://vacationtracker.io/developers/api/users/listUsers) |
