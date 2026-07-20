# TalentLyft: Native API Reference

A consolidated summary of TalentLyft's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://developers.talentlyft.com/
- **OpenAPI specification:** https://api.talentlyft.com/swagger/index.html
- **API base URL:** `https://api.talentlyft.com`

## Authentication

### API Key

Connect TalentLyft with a TalentLyft access token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.talentlyft.com/authorization-types)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Department](actions/create-department.md) | `POST /v2/departments` | [docs](https://developers.talentlyft.com/customer-api-reference/departments) |
| [Create Rejection Reason](actions/create-rejection-reason.md) | `POST /v2/rejection_reasons` | [docs](https://developers.talentlyft.com/customer-api-reference/rejection-reasons) |
| [Delete Department](actions/delete-department.md) | `DELETE /v2/departments/:id` | [docs](https://developers.talentlyft.com/customer-api-reference/departments) |
| [Delete Rejection Reason](actions/delete-rejection-reason.md) | `DELETE /v2/rejection_reasons/:id` | [docs](https://developers.talentlyft.com/customer-api-reference/rejection-reasons) |
| [Get Articles](actions/get-articles.md) | `GET /v2/articles` | [docs](https://developers.talentlyft.com/customer-api-reference/articles) |
| [Get Department](actions/get-department.md) | `GET /v2/departments/:id` | [docs](https://developers.talentlyft.com/customer-api-reference/departments) |
| [Get Department By External ID](actions/get-department-by-external-id.md) | `GET /v2/departments/:id/external` | [docs](https://developers.talentlyft.com/customer-api-reference/departments) |
| [Get Departments](actions/get-departments.md) | `GET /v2/departments` | [docs](https://developers.talentlyft.com/customer-api-reference/departments) |
| [Get Employees](actions/get-employees.md) | `GET /v2/employees` | [docs](https://developers.talentlyft.com/customer-api-reference/employees) |
| [Get Forms](actions/get-forms.md) | `GET /v2/forms` | [docs](https://developers.talentlyft.com/customer-api-reference/forms) |
| [Get Job Locations](actions/get-job-locations.md) | `GET /v2/jobs/locations` | [docs](https://developers.talentlyft.com/customer-api-reference/jobs) |
| [Get Jobs](actions/get-jobs.md) | `GET /v2/jobs` | [docs](https://developers.talentlyft.com/customer-api-reference/jobs) |
| [Get Meetings](actions/get-meetings.md) | `GET /v2/events` | [docs](https://developers.talentlyft.com/customer-api-reference/events) |
| [Get Pipeline](actions/get-pipeline.md) | `GET /v2/pipelines/:id` | [docs](https://developers.talentlyft.com/customer-api-reference/pipelines) |
| [Get Pipelines](actions/get-pipelines.md) | `GET /v2/pipelines` | [docs](https://developers.talentlyft.com/customer-api-reference/pipelines) |
| [Get Rejection Reason](actions/get-rejection-reason.md) | `GET /v2/rejection_reasons/:id` | [docs](https://developers.talentlyft.com/customer-api-reference/rejection-reasons) |
| [Get Rejection Reasons](actions/get-rejection-reasons.md) | `GET /v2/rejection_reasons` | [docs](https://developers.talentlyft.com/customer-api-reference/rejection-reasons) |
| [List Members](actions/list-members.md) | `GET /v2/members` | [docs](https://developers.talentlyft.com/customer-api-reference/members) |
| [Update Department](actions/update-department.md) | `PUT /v2/departments/:id` | [docs](https://developers.talentlyft.com/customer-api-reference/departments) |
| [Update Rejection Reason](actions/update-rejection-reason.md) | `PUT /v2/rejection_reasons/:id` | [docs](https://developers.talentlyft.com/customer-api-reference/rejection-reasons) |
