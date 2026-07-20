# Recooty: Native API Reference

A consolidated summary of Recooty's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://api.recooty.com/
- **API base URL:** `https://standaloneapi.recooty.app/api`

## Authentication

### Recooty API Credentials

Use your Recooty public API key for job listing endpoints. Add a personal access token if you also want to call candidate endpoints.

### Credentials

- **Job Listing Key:** `jobListingKey` · required · The Recooty Job Listing API key used only in the /v1/jobs/{key} path segment.
- **Personal Access Token:** `accessToken` · optional · Optional Recooty personal access token used only for candidate endpoints with Authorization: Bearer <token>.

Send these headers with each API request:

```http
Authorization: Bearer <accessToken>
```

[Official authentication documentation](https://api.recooty.com/)

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Application](actions/create-application.md) | `POST /v1/jobs/{{jobId}}/application` | [docs](https://api.recooty.com/) |
| [Get Application](actions/get-application.md) | `GET /v1/applications/{{applicationId}}` | [docs](https://api.recooty.com/) |
| [Get Job](actions/get-job.md) | `GET /v1/jobs/{{credentials.jobListingKey}}/{{jobId}}` | [docs](https://api.recooty.com/) |
| [List Applications](actions/list-applications.md) | `GET /v1/jobs/{{jobId}}/applications` | [docs](https://api.recooty.com/) |
| [List Jobs](actions/list-jobs.md) | `GET /v1/jobs/{{credentials.jobListingKey}}` | [docs](https://api.recooty.com/) |
