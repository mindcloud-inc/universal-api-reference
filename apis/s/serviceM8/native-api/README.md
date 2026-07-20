# ServiceM8: Native API Reference

A consolidated summary of ServiceM8's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://developer.servicem8.com/docs/rest-overview
- **API base URL:** `https://api.servicem8.com`

## Authentication

### API Key

Authenticate requests with a ServiceM8 API key sent in the X-API-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://developer.servicem8.com/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `cursor` in the query string as the pagination cursor; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `eq`, `gt`, `lt`, `ne`.

## Sorting

Set the sort field with `$sort` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | `POST /api_1.0/company.json` | [docs](https://developer.servicem8.com/reference/createclients) |
| [Create Company Contact](actions/create-company-contact.md) | `POST /api_1.0/companycontact.json` | [docs](https://developer.servicem8.com/reference/createcompanycontacts) |
| [Create Job](actions/create-job.md) | `POST /api_1.0/job.json` | [docs](https://developer.servicem8.com/reference/createjobs) |
| [Create Job Activity](actions/create-job-activity.md) | `POST /api_1.0/jobactivity.json` | [docs](https://developer.servicem8.com/reference/createjobactivities) |
| [Create Job Allocation](actions/create-job-allocation.md) | `POST /api_1.0/joballocation.json` | [docs](https://developer.servicem8.com/reference/createjoballocations) |
| [Create Task](actions/create-task.md) | `POST /api_1.0/task.json` | [docs](https://developer.servicem8.com/reference/createtasks) |
| [Get Client](actions/get-client.md) | `GET /api_1.0/company/:uuid.json` | [docs](https://developer.servicem8.com/reference/getclients) |
| [Get Job](actions/get-job.md) | `GET /api_1.0/job/:uuid.json` | [docs](https://developer.servicem8.com/reference/getjobs) |
| [Get Staff Member](actions/get-staff-member.md) | `GET /api_1.0/staff/:uuid.json` | [docs](https://developer.servicem8.com/reference/getstaffmembers) |
| [List Clients](actions/list-clients.md) | `GET /api_1.0/company.json` | [docs](https://developer.servicem8.com/reference/listclients) |
| [List Company Contacts](actions/list-company-contacts.md) | `GET /api_1.0/companycontact.json` | [docs](https://developer.servicem8.com/reference/listcompanycontacts) |
| [List Job Activities](actions/list-job-activities.md) | `GET /api_1.0/jobactivity.json` | [docs](https://developer.servicem8.com/reference/listjobactivities) |
| [List Job Allocations](actions/list-job-allocations.md) | `GET /api_1.0/joballocation.json` | [docs](https://developer.servicem8.com/reference/listjoballocations) |
| [List Jobs](actions/list-jobs.md) | `GET /api_1.0/job.json` | [docs](https://developer.servicem8.com/reference/listjobs) |
| [List Staff Members](actions/list-staff-members.md) | `GET /api_1.0/staff.json` | [docs](https://developer.servicem8.com/reference/liststaffmembers) |
| [List Tasks](actions/list-tasks.md) | `GET /api_1.0/task.json` | [docs](https://developer.servicem8.com/reference/listtasks) |
| [Update Client](actions/update-client.md) | `POST /api_1.0/company/:uuid.json` | [docs](https://developer.servicem8.com/reference/updateclients) |
| [Update Company Contact](actions/update-company-contact.md) | `POST /api_1.0/companycontact/:uuid.json` | [docs](https://developer.servicem8.com/reference/updatecompanycontacts) |
| [Update Job](actions/update-job.md) | `POST /api_1.0/job/:uuid.json` | [docs](https://developer.servicem8.com/reference/updatejobs) |
| [Update Job Activity](actions/update-job-activity.md) | `POST /api_1.0/jobactivity/:uuid.json` | [docs](https://developer.servicem8.com/reference/updatejobactivities) |
| [Update Staff Member](actions/update-staff-member.md) | `POST /api_1.0/staff/:uuid.json` | [docs](https://developer.servicem8.com/reference/updatestaffmembers) |
| [Update Task](actions/update-task.md) | `POST /api_1.0/task/:uuid.json` | [docs](https://developer.servicem8.com/reference/updatetasks) |
