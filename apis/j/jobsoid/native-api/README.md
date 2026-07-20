# Jobsoid: Native API Reference

A consolidated summary of Jobsoid's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.jobsoid.com/
- **OpenAPI specification:** https://apidocs.jobsoid.com/jobsoid.json
- **API base URL:** `https://demo.jobsoid.com`

## Authentication

### No authentication

Jobsoid's public applicant API endpoints do not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://apidocs.jobsoid.com/)

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get job](actions/get-job.md) | `GET /api/v1/jobs/{{jobId}}` | [docs](https://apidocs.jobsoid.com/) |
| [List departments](actions/list-departments.md) | `GET /api/v1/departments` | [docs](https://apidocs.jobsoid.com/) |
| [List divisions](actions/list-divisions.md) | `GET /api/v1/divisions` | [docs](https://apidocs.jobsoid.com/) |
| [List job functions](actions/list-job-functions.md) | `GET /api/v1/functions` | [docs](https://apidocs.jobsoid.com/) |
| [List jobs](actions/list-jobs.md) | `GET /api/v1/jobs` | [docs](https://apidocs.jobsoid.com/) |
| [List locations](actions/list-locations.md) | `GET /api/v1/locations` | [docs](https://apidocs.jobsoid.com/) |
