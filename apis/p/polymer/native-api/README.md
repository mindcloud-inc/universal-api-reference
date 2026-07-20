# Polymer: Native API Reference

A consolidated summary of Polymer's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://developer.polymer.co/
- **API base URL:** `https://api.polymer.co/v1/hire`

## Authentication

### API Key

Authenticate to Polymer Customer API with an API key in the Authorization bearer header.

### Credentials

- **API key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.polymer.co/#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 50; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Apply For Job](actions/apply-for-job.md) | `POST /job_applications/apply` | [docs](https://developer.polymer.co/#apply-for-a-job) |
| [Archive Job Application](actions/archive-job-application.md) | `POST /job_applications/:job_application_id/archive` | [docs](https://developer.polymer.co/#archive) |
| [Create Job Application Comment](actions/create-job-application-comment.md) | `POST /job_applications/:job_application_id/comments` | [docs](https://developer.polymer.co/#create-a-comment) |
| [Create Job Application Review](actions/create-job-application-review.md) | `POST /job_applications/:job_application_id/reviews` | [docs](https://developer.polymer.co/#create-a-review) |
| [Delete Job Application Comment](actions/delete-job-application-comment.md) | `DELETE /job_applications/:job_application_id/comments/:comment_id` | [docs](https://developer.polymer.co/#delete-a-comment) |
| [Delete Job Application Review](actions/delete-job-application-review.md) | `DELETE /job_applications/:job_application_id/reviews/:review_id` | [docs](https://developer.polymer.co/#delete-a-review) |
| [Get Candidate](actions/get-candidate.md) | `GET /candidates/:candidate_id` | [docs](https://developer.polymer.co/#get-a-candidate) |
| [Get Candidate With Applications](actions/get-candidate-with-applications.md) | `GET /candidates/:candidate_id` | [docs](https://developer.polymer.co/#get-a-candidate-with-job-applications) |
| [Get Hiring Stage Events](actions/get-hiring-stage-events.md) | `GET /job_applications/:job_application_id/hiring_stage_events` | [docs](https://developer.polymer.co/#get-hiring-stage-events) |
| [Get Hiring Stages](actions/get-hiring-stages.md) | `GET /jobs/:job_id/hiring_stages` | [docs](https://developer.polymer.co/#get-hiring-stages) |
| [Get Job](actions/get-job.md) | `GET /jobs/:job_id` | [docs](https://developer.polymer.co/#get-a-job) |
| [Get Job Application](actions/get-job-application.md) | `GET /job_applications/:job_application_id` | [docs](https://developer.polymer.co/#get-a-job-application) |
| [Get Job Application Comments](actions/get-job-application-comments.md) | `GET /job_applications/:job_application_id/comments` | [docs](https://developer.polymer.co/#get-job-application-comments) |
| [Get Job Application Messages](actions/get-job-application-messages.md) | `GET /job_applications/:job_application_id/messages` | [docs](https://developer.polymer.co/#get-job-application-messages) |
| [Get Job Application Reviews](actions/get-job-application-reviews.md) | `GET /job_applications/:job_application_id/reviews` | [docs](https://developer.polymer.co/#get-job-application-reviews) |
| [Get Organization](actions/get-organization.md) | `GET /organization` | [docs](https://developer.polymer.co/#get-organization) |
| [Get Organization User](actions/get-organization-user.md) | `GET /organization_users/:organization_user_id` | [docs](https://developer.polymer.co/#get-an-organization-user) |
| [Get Resume Export](actions/get-resume-export.md) | `GET /jobs/:job_id/resume_export_job` | [docs](https://developer.polymer.co/#get-resume-export) |
| [Import Job Application](actions/import-job-application.md) | `POST /job_applications/import` | [docs](https://developer.polymer.co/#import-a-job-application) |
| [List Active Users](actions/list-active-users.md) | `GET /organization_users/active` | [docs](https://developer.polymer.co/#list-active-users) |
| [List Candidates](actions/list-candidates.md) | `GET /candidates` | [docs](https://developer.polymer.co/#list-candidates) |
| [List Deactivated Users](actions/list-deactivated-users.md) | `GET /organization_users/deactivated` | [docs](https://developer.polymer.co/#list-deactivated-users) |
| [List Job Applications](actions/list-job-applications.md) | `GET /job_applications` | [docs](https://developer.polymer.co/#list-job-applications) |
| [List Jobs](actions/list-jobs.md) | `GET /jobs` | [docs](https://developer.polymer.co/#list-jobs) |
| [Move Job Application Stage](actions/move-job-application-stage.md) | `POST /job_applications/:job_application_id/move_stage` | [docs](https://developer.polymer.co/#move-stage) |
| [Start Resume Export](actions/start-resume-export.md) | `POST /jobs/:job_id/resume_export_job` | [docs](https://developer.polymer.co/#start-resume-export) |
| [Update Job Application Comment](actions/update-job-application-comment.md) | `PUT /job_applications/:job_application_id/comments/:comment_id` | [docs](https://developer.polymer.co/#update-a-comment) |
| [Update Job Application Review](actions/update-job-application-review.md) | `PUT /job_applications/:job_application_id/reviews/:review_id` | [docs](https://developer.polymer.co/#update-a-review) |
