# 100Hires ATS: Native API Reference

A consolidated summary of 100Hires ATS's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://100hires.com/api
- **OpenAPI specification:** https://api.100hires.com/v2/openapi.json
- **API base URL:** `https://api.100hires.com/v2`

## Authentication

### Bearer Token

Authenticate with a 100Hires API token sent as a Bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://100hires.com/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `users`. The total page count is read from `pagination.page_count`. The current page number is read from `pagination.page`.

## Pagination

Use `size` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Hiring Team Member](actions/add-hiring-team-member.md) | `POST /jobs/:id/hiring-team` | [docs](https://100hires.com/api) |
| [Advance Application To Next Stage](actions/advance-application-to-next-stage.md) | `POST /applications/:id/advance` | [docs](https://100hires.com/api) |
| [Batch Add Tags To Candidates](actions/batch-add-tags-to-candidates.md) | `POST /candidates/batch/tags` | [docs](https://100hires.com/api) |
| [Batch Remove Tags From Candidates](actions/batch-remove-tags-from-candidates.md) | `DELETE /candidates/batch/tags` | [docs](https://100hires.com/api) |
| [Create Application](actions/create-application.md) | `POST /applications` | [docs](https://100hires.com/api) |
| [Create Candidate](actions/create-candidate.md) | `POST /candidates` | [docs](https://100hires.com/api) |
| [Create Interview](actions/create-interview.md) | `POST /applications/:id/interviews` | [docs](https://100hires.com/api) |
| [Create Job](actions/create-job.md) | `POST /jobs` | [docs](https://100hires.com/api) |
| [Get Application](actions/get-application.md) | `GET /applications/:id` | [docs](https://100hires.com/api) |
| [Get Application AI Score](actions/get-application-ai-score.md) | `GET /applications/:id/ai-score` | [docs](https://100hires.com/api) |
| [Get Candidate](actions/get-candidate.md) | `GET /candidates/:id` | [docs](https://100hires.com/api) |
| [Get Job](actions/get-job.md) | `GET /jobs/:id` | [docs](https://100hires.com/api) |
| [Get User](actions/get-user.md) | `GET /users/:id` | [docs](https://100hires.com/api) |
| [List Application Evaluation Forms](actions/list-application-evaluation-forms.md) | `GET /applications/:id/evaluation-forms` | [docs](https://100hires.com/api) |
| [List Applications](actions/list-applications.md) | `GET /applications` | [docs](https://100hires.com/api) |
| [List Candidate Activities](actions/list-candidate-activities.md) | `GET /candidates/:id/activities` | [docs](https://100hires.com/api) |
| [List Candidates](actions/list-candidates.md) | `GET /candidates` | [docs](https://100hires.com/api) |
| [List Company Tags](actions/list-company-tags.md) | `GET /tags` | [docs](https://100hires.com/api) |
| [List Job Hiring Team](actions/list-job-hiring-team.md) | `GET /jobs/:id/hiring-team` | [docs](https://100hires.com/api) |
| [List Jobs](actions/list-jobs.md) | `GET /jobs` | [docs](https://100hires.com/api) |
| [List Rejection Reasons](actions/list-rejection-reasons.md) | `GET /rejection-reasons` | [docs](https://100hires.com/api) |
| [List User Mail Accounts](actions/list-user-mail-accounts.md) | `GET /users/:id/mail-accounts` | [docs](https://100hires.com/api) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://100hires.com/api) |
| [List Workflow Stages](actions/list-workflow-stages.md) | `GET /workflows/stages` | [docs](https://100hires.com/api) |
| [List Workflows](actions/list-workflows.md) | `GET /workflows` | [docs](https://100hires.com/api) |
| [Mark Application As Hired](actions/mark-application-as-hired.md) | `POST /applications/:id/hire` | [docs](https://100hires.com/api) |
| [Move Application To Stage](actions/move-application-to-stage.md) | `POST /applications/:id/move` | [docs](https://100hires.com/api) |
| [Reject Application](actions/reject-application.md) | `POST /applications/:id/reject` | [docs](https://100hires.com/api) |
| [Transfer Application To Another Job](actions/transfer-application-to-another-job.md) | `POST /applications/:id/transfer` | [docs](https://100hires.com/api) |
| [Update Application](actions/update-application.md) | `PUT /applications/:id` | [docs](https://100hires.com/api) |
| [Update Candidate](actions/update-candidate.md) | `PUT /candidates/:id` | [docs](https://100hires.com/api) |
| [Update Job](actions/update-job.md) | `PUT /jobs/:id` | [docs](https://100hires.com/api) |
| [Update Job Status](actions/update-job-status.md) | `POST /jobs/:id/status` | [docs](https://100hires.com/api) |
