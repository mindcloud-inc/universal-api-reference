# HRBLADE: Native API Reference

A consolidated summary of HRBLADE's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://hrblade.com/docs/developers/api-reference
- **OpenAPI specification:** https://documenter.getpostman.com/view/15055534/TzCFgWPB
- **API base URL:** `https://api.hrblade.com/api`

## Authentication

### API Key

Use the API key generated in HRBLADE Profile > Integrations.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://hrblade.com/docs/user-documentation/generate-api-key-for-integrations)

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | `POST /company/create` | [docs](https://documenter.getpostman.com/view/15055534/TzCFgWPB) |
| [Create Job](actions/create-job.md) | `POST /job/create` | [docs](https://documenter.getpostman.com/view/15055534/TzCFgWPB) |
| [Get Company](actions/get-company.md) | `GET /company/get/:id` | [docs](https://documenter.getpostman.com/view/15055534/TzCFgWPB) |
| [Get Config](actions/get-config.md) | `GET /config` | [docs](https://documenter.getpostman.com/view/15055534/TzCFgWPB) |
| [Get Job](actions/get-job.md) | `GET /job/get/:id` | [docs](https://documenter.getpostman.com/view/15055534/TzCFgWPB) |
| [Get Response](actions/get-response.md) | `GET /response/get/:id` | [docs](https://documenter.getpostman.com/view/15055534/TzCFgWPB) |
| [Get User](actions/get-user.md) | `GET /user` | [docs](https://documenter.getpostman.com/view/15055534/TzCFgWPB) |
| [Invite Candidates By Email](actions/invite-candidates-by-email.md) | `POST /job/invite/create` | [docs](https://documenter.getpostman.com/view/15055534/TzCFgWPB) |
| [List Companies](actions/list-companies.md) | `GET /companies` | [docs](https://documenter.getpostman.com/view/15055534/TzCFgWPB) |
| [List Jobs](actions/list-jobs.md) | `GET /jobs` | [docs](https://documenter.getpostman.com/view/15055534/TzCFgWPB) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://documenter.getpostman.com/view/15055534/TzCFgWPB) |
| [Login](actions/login.md) | `POST /login` | [docs](https://documenter.getpostman.com/view/15055534/TzCFgWPB) |
| [Remove Job](actions/remove-job.md) | `POST /job/remove/:id` | [docs](https://documenter.getpostman.com/view/15055534/TzCFgWPB) |
| [Update Company](actions/update-company.md) | `POST /company/update` | [docs](https://documenter.getpostman.com/view/15055534/TzCFgWPB) |
| [Update Job](actions/update-job.md) | `POST /job/update` | [docs](https://documenter.getpostman.com/view/15055534/TzCFgWPB) |
| [Update Job Status](actions/update-job-status.md) | `POST /job/active` | [docs](https://documenter.getpostman.com/view/15055534/TzCFgWPB) |
| [Update Response Rating](actions/update-response-rating.md) | `POST /response/add/rating` | [docs](https://documenter.getpostman.com/view/15055534/TzCFgWPB) |
| [Update Response Status](actions/update-response-status.md) | `POST /response/change/status` | [docs](https://documenter.getpostman.com/view/15055534/TzCFgWPB) |
| [Update User Settings](actions/update-user-settings.md) | `POST /user/settings` | [docs](https://documenter.getpostman.com/view/15055534/TzCFgWPB) |
