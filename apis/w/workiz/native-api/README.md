# Workiz: Native API Reference

A consolidated summary of Workiz's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://developer.workiz.com/
- **OpenAPI specification:** https://developer.workiz.com/api.json
- **API base URL:** `https://api.workiz.com/api/v1/{apiKey}`

## Authentication

### API Key

Connect Workiz with your API token and API secret.

### Credentials

- **API Key:** `apiKey` · required
- **API Secret:** `authSecret` · required · Workiz API secret used on mutating requests.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.workiz.com/hc/en-us/articles/18053137531409-Accessing-your-Workiz-API-credentials)

## API conventions

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `records` in the query string to set the page size (default 100; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate Lead](actions/activate-lead.md) | `POST /lead/activate/:UUID/` | [docs](https://developer.workiz.com/) |
| [Add Job Payment](actions/add-job-payment.md) | `POST /job/addPayment/:UUID/` | [docs](https://developer.workiz.com/) |
| [Assign User to Job](actions/assign-user-to-job.md) | `POST /job/assign/` | [docs](https://developer.workiz.com/) |
| [Assign User to Lead](actions/assign-user-to-lead.md) | `POST /lead/assign/` | [docs](https://developer.workiz.com/) |
| [Convert Lead To Job](actions/convert-lead-to-job.md) | `POST /lead/convert/` | [docs](https://developer.workiz.com/) |
| [Create Job](actions/create-job.md) | `POST /job/create/` | [docs](https://developer.workiz.com/) |
| [Create Lead](actions/create-lead.md) | `POST /lead/create/` | [docs](https://developer.workiz.com/) |
| [Get Job](actions/get-job.md) | `GET /job/get/:UUID/` | [docs](https://developer.workiz.com/#/Jobs/getJob) |
| [Get Lead](actions/get-lead.md) | `GET /lead/get/:UUID/` | [docs](https://developer.workiz.com/#/Leads/getJob) |
| [Get Team Member](actions/get-team-member.md) | `GET /team/get/:USER_ID/` | [docs](https://developer.workiz.com/#/Team/getUser) |
| [List Jobs](actions/list-jobs.md) | `GET /job/all/` | [docs](https://developer.workiz.com/#/Jobs/getJobs) |
| [List Leads](actions/list-leads.md) | `GET /lead/all/` | [docs](https://developer.workiz.com/#/Leads/getLeads) |
| [List Team Members](actions/list-team-members.md) | `GET /team/all/` | [docs](https://developer.workiz.com/#/Team/getTeam) |
| [List Time Offs](actions/list-time-offs.md) | `GET /TimeOff/get/` | [docs](https://developer.workiz.com/#/Time Off/getTimeOff) |
| [List Time Offs by User](actions/list-time-offs-by-user.md) | `GET /TimeOff/get/:USER_NAME` | [docs](https://developer.workiz.com/#/Time Off/getUserTimeOff) |
| [Mark Lead Lost](actions/mark-lead-lost.md) | `POST /lead/markLost/:UUID/` | [docs](https://developer.workiz.com/) |
| [Unassign User from Job](actions/unassign-user-from-job.md) | `POST /job/unassign/` | [docs](https://developer.workiz.com/) |
| [Unassign User from Lead](actions/unassign-user-from-lead.md) | `POST /lead/unassign/` | [docs](https://developer.workiz.com/) |
| [Update Job](actions/update-job.md) | `POST /job/update/` | [docs](https://developer.workiz.com/) |
| [Update Lead](actions/update-lead.md) | `POST /lead/update/` | [docs](https://developer.workiz.com/) |
