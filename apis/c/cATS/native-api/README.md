# CATS: Native API Reference

A consolidated summary of CATS's API configuration and 45 documented operations, with links to official documentation.

- **Official docs:** https://docs.catsone.com/api/v3/
- **API base URL:** `https://api.catsone.com/v3`

## Authentication

### API Key

Authenticate with a CATS v3 API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.catsone.com/api/v3/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 25; maximum 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (45 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Change Job Status](actions/change-job-status.md) | `POST /jobs/:id/status` | [docs](https://docs.catsone.com/api/v3/#jobs-change-job-status) |
| [Change Pipeline Status](actions/change-pipeline-status.md) | `POST /pipelines/:id/status` | [docs](https://docs.catsone.com/api/v3/#pipelines-change-pipeline-status) |
| [Create Candidate](actions/create-candidate.md) | `POST /candidates` | [docs](https://docs.catsone.com/api/v3/#candidates-create-a-candidate) |
| [Create Candidate Activity](actions/create-candidate-activity.md) | `POST /candidates/:id/activities` | [docs](https://docs.catsone.com/api/v3/#candidates-create-a-candidate-activity) |
| [Create Company](actions/create-company.md) | `POST /companies` | [docs](https://docs.catsone.com/api/v3/#companies-create-a-company) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://docs.catsone.com/api/v3/#contacts-create-a-contact) |
| [Create Job](actions/create-job.md) | `POST /jobs` | [docs](https://docs.catsone.com/api/v3/#jobs-create-a-job) |
| [Create Pipeline](actions/create-pipeline.md) | `POST /pipelines` | [docs](https://docs.catsone.com/api/v3/#pipelines-create-a-pipeline) |
| [Delete Candidate](actions/delete-candidate.md) | `DELETE /candidates/:id` | [docs](https://docs.catsone.com/api/v3/#candidates-delete-a-candidate) |
| [Delete Company](actions/delete-company.md) | `DELETE /companies/:id` | [docs](https://docs.catsone.com/api/v3/#companies-delete-a-company) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:id` | [docs](https://docs.catsone.com/api/v3/#contacts-delete-a-contact) |
| [Delete Job](actions/delete-job.md) | `DELETE /jobs/:id` | [docs](https://docs.catsone.com/api/v3/#jobs-delete-a-job) |
| [Delete Pipeline](actions/delete-pipeline.md) | `DELETE /pipelines/:id` | [docs](https://docs.catsone.com/api/v3/#pipelines-delete-a-pipeline) |
| [Filter Candidates](actions/filter-candidates.md) | `POST /candidates/search` | [docs](https://docs.catsone.com/api/v3/#candidates-filter-candidates) |
| [Filter Jobs](actions/filter-jobs.md) | `POST /jobs/search` | [docs](https://docs.catsone.com/api/v3/#jobs-filter-jobs) |
| [Filter Pipelines](actions/filter-pipelines.md) | `POST /pipelines/search` | [docs](https://docs.catsone.com/api/v3/#pipelines-filter-pipelines) |
| [Get Candidate](actions/get-candidate.md) | `GET /candidates/:id` | [docs](https://docs.catsone.com/api/v3/#candidates-get-a-candidate) |
| [Get Candidate Application](actions/get-candidate-application.md) | `GET /candidates/applications/:application_id` | [docs](https://docs.catsone.com/api/v3/#candidates-get-a-candidate-application) |
| [Get Company](actions/get-company.md) | `GET /companies/:id` | [docs](https://docs.catsone.com/api/v3/#companies-get-a-company) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id` | [docs](https://docs.catsone.com/api/v3/#contacts-get-a-contact) |
| [Get Job](actions/get-job.md) | `GET /jobs/:id` | [docs](https://docs.catsone.com/api/v3/#jobs-get-a-job) |
| [Get Job Application](actions/get-job-application.md) | `GET /jobs/applications/:application_id` | [docs](https://docs.catsone.com/api/v3/#jobs-get-a-job-application) |
| [Get Pipeline](actions/get-pipeline.md) | `GET /pipelines/:id` | [docs](https://docs.catsone.com/api/v3/#pipelines-get-a-pipeline) |
| [Get Site](actions/get-site.md) | `GET /site` | [docs](https://docs.catsone.com/api/v3/#site-get-site) |
| [List Applications By Candidate](actions/list-applications-by-candidate.md) | `GET /candidates/:candidate_id/applications` | [docs](https://docs.catsone.com/api/v3/#candidates-list-applications-by-candidate) |
| [List Applications By Job](actions/list-applications-by-job.md) | `GET /jobs/:job_id/applications` | [docs](https://docs.catsone.com/api/v3/#jobs-list-applications-by-job) |
| [List Candidate Activities](actions/list-candidate-activities.md) | `GET /candidates/:id/activities` | [docs](https://docs.catsone.com/api/v3/#candidates-list-candidate-activities) |
| [List Candidates](actions/list-candidates.md) | `GET /candidates` | [docs](https://docs.catsone.com/api/v3/#candidates-list-all-candidates) |
| [List Companies](actions/list-companies.md) | `GET /companies` | [docs](https://docs.catsone.com/api/v3/#companies-list-all-companies) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://docs.catsone.com/api/v3/#contacts-list-all-contacts) |
| [List Job Statuses](actions/list-job-statuses.md) | `GET /jobs/statuses` | [docs](https://docs.catsone.com/api/v3/#jobs-list-job-statuses) |
| [List Jobs](actions/list-jobs.md) | `GET /jobs` | [docs](https://docs.catsone.com/api/v3/#jobs-list-all-jobs) |
| [List Pipelines](actions/list-pipelines.md) | `GET /pipelines` | [docs](https://docs.catsone.com/api/v3/#pipelines-list-all-pipelines) |
| [List Pipelines By Candidate](actions/list-pipelines-by-candidate.md) | `GET /candidates/:id/pipelines` | [docs](https://docs.catsone.com/api/v3/#candidates-list-pipelines-by-candidate) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://docs.catsone.com/api/v3/#users-list-all-users) |
| [Search Candidates](actions/search-candidates.md) | `GET /candidates/search` | [docs](https://docs.catsone.com/api/v3/#candidates-search-candidates) |
| [Search Companies](actions/search-companies.md) | `GET /companies/search` | [docs](https://docs.catsone.com/api/v3/#companies-search-companies) |
| [Search Contacts](actions/search-contacts.md) | `GET /contacts/search` | [docs](https://docs.catsone.com/api/v3/#contacts-search-contacts) |
| [Search Jobs](actions/search-jobs.md) | `GET /jobs/search` | [docs](https://docs.catsone.com/api/v3/#jobs-search-jobs) |
| [Update Candidate](actions/update-candidate.md) | `PUT /candidates/:id` | [docs](https://docs.catsone.com/api/v3/#candidates-update-a-candidate) |
| [Update Company](actions/update-company.md) | `PUT /companies/:id` | [docs](https://docs.catsone.com/api/v3/#companies-update-a-company) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:id` | [docs](https://docs.catsone.com/api/v3/#contacts-update-a-contact) |
| [Update Job](actions/update-job.md) | `PUT /jobs/:id` | [docs](https://docs.catsone.com/api/v3/#jobs-update-a-job) |
| [Update Pipeline](actions/update-pipeline.md) | `PUT /pipelines/:id` | [docs](https://docs.catsone.com/api/v3/#pipelines-update-a-pipeline) |
| [Upload Resume](actions/upload-resume.md) | `POST /candidates/:id/resumes` | [docs](https://docs.catsone.com/api/v3/#candidates-upload-a-resume) |
