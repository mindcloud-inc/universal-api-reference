# NeverBounce: Native API Reference

A consolidated summary of NeverBounce's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://developers.neverbounce.com/reference/getting-started
- **API base URL:** `https://api.neverbounce.com/v4.2`

## Authentication

### API Key

Authenticate NeverBounce requests with your API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.neverbounce.com/reference/authentication)

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Job From Remote URL](actions/create-job-from-remote-url.md) | `POST /jobs/create` | [docs](https://developers.neverbounce.com/reference/jobs-create) |
| [Create Job From Supplied Data](actions/create-job-from-supplied-data.md) | `POST /jobs/create` | [docs](https://developers.neverbounce.com/reference/jobs-create) |
| [Delete Job](actions/delete-job.md) | `POST /jobs/delete` | [docs](https://developers.neverbounce.com/reference/jobs-delete) |
| [Download Job Results](actions/download-job-results.md) | `GET /jobs/download` | [docs](https://developers.neverbounce.com/reference/jobs-download) |
| [Get Account Info](actions/get-account-info.md) | `GET /account/info` | [docs](https://developers.neverbounce.com/reference/account-info) |
| [Get Job Results](actions/get-job-results.md) | `GET /jobs/results` | [docs](https://developers.neverbounce.com/reference/jobs-results) |
| [Get Job Status](actions/get-job-status.md) | `GET /jobs/status` | [docs](https://developers.neverbounce.com/reference/jobs-status) |
| [Parse Job](actions/parse-job.md) | `POST /jobs/parse` | [docs](https://developers.neverbounce.com/reference/jobs-parse) |
| [Search Jobs](actions/search-jobs.md) | `GET /jobs/search` | [docs](https://developers.neverbounce.com/reference/jobs-search) |
| [Start Job](actions/start-job.md) | `POST /jobs/start` | [docs](https://developers.neverbounce.com/reference/jobs-start) |
| [Verify Email](actions/verify-email.md) | `GET /single/check` | [docs](https://developers.neverbounce.com/reference/single-check) |
