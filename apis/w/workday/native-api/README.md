# Workday: Native API Reference

A consolidated summary of Workday's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://community.workday.com/sites/default/files/file-hosting/restapi/index.html
- **API base URL:** `{restAPIBaseURL}/`

## Authentication

### Custom

### Credentials

- **Time Tracking REST API Base URL:** `restAPIBaseURL` · required · Use the full Workday timeTracking v5 service base URL for your tenant, for example: https://services1.wd501.myworkday.com/ccx/api/timeTracking/v5/marianienterprises
- **Token Endpoint:** `tokenEndpoint` · optional · This looks something like: 
https://services1.wd501.myworkday.com/ccx/oauth2/mycompany/token
- **Client ID:** `clientID` · optional
- **Client Secret:** `clientSecret` · optional
- **Refresh Token:** `refreshToken` · optional
- **Person REST API Base URL:** `personRestAPIBaseURL` · required · Use the full Workday person v4 service base URL for your tenant, for example: https://services1.wd501.myworkday.com/ccx/api/person/v4/marianienterprises
- **Tenant:** `tenant` · optional · If your REST API endpoint is https://services1.wd501.myworkday.com/ccx/api/v1/mycompany,
then your tenant is "mycompany"

Send these headers with each API request:

```http
Authorization: Bearer <custom.accessToken>
```

## Pagination

Use `limit` in the query string to set the page size (default 100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Timesheet Entry](actions/create-timesheet-entry.md) | `POST workers/:ID/workerTimeBlock` | [docs](https://community.workday.com/sites/default/files/file-hosting/restapi/index.html#timeTracking/v5/post-/workers/-ID-/workerTimeBlock) |
| [Get Job Profiles](actions/get-job-profiles.md) | `GET jobProfiles/:ID` | [docs](https://community.workday.com/sites/default/files/file-hosting/restapi/index.html#timeTracking/v5/get-/workers/-ID-) |
| [Get Person](actions/get-person.md) | `GET people/:ID` | [docs](https://community.workday.com/sites/default/files/file-hosting/restapi/index.html#person/v4/get-/people/-ID-) |
| [Get Token](actions/get-token.md) | `POST {{credentials.tokenEndpoint}}` |  |
| [Get Worker](actions/get-worker.md) | `GET workers/:ID` | [docs](https://community.workday.com/sites/default/files/file-hosting/restapi/index.html#timeTracking/v5/get-/workers/-ID-) |
| [Get Workers](actions/get-workers.md) | `GET workers` | [docs](https://community.workday.com/sites/default/files/file-hosting/restapi/index.html#timeTracking/v5/get-/workers) |
| [Get Workers History](actions/get-workers-history.md) | `GET workers/:ID/history` | [docs](https://community.workday.com/sites/default/files/file-hosting/restapi/index.html#timeTracking/v5/get-/workers) |
| [List People](actions/list-people.md) | `GET people` | [docs](https://community.workday.com/sites/default/files/file-hosting/restapi/index.html#person/v4/get-/people) |
| [List Time Tracking Workers](actions/list-time-tracking-workers.md) | `GET workers` | [docs](https://community.workday.com/sites/default/files/file-hosting/restapi/index.html#timeTracking/v5/get-/workers) |
| [List Worker Organizations](actions/list-worker-organizations.md) | `GET workers/:ID/organizations` | [docs](https://community.workday.com/sites/default/files/file-hosting/restapi/index.html#timeTracking/v5/get-/workers/-ID-) |
| [List Worker Time Blocks](actions/list-worker-time-blocks.md) | `GET /workerTimeBlocks` | [docs](https://community.workday.com/sites/default/files/file-hosting/restapi/index.html#timeTracking/v5/get-/workerTimeBlocks) |
| [Update Timesheet Entry](actions/update-timesheet-entry.md) | `PATCH workers/:ID/workerTimeBlock/:subresourceID` | [docs](https://community.workday.com/sites/default/files/file-hosting/restapi/index.html#timeTracking/v5/patch-/workers/-ID-/workerTimeBlock/-subresourceID-) |
