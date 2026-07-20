# PickFu: Native API Reference

A consolidated summary of PickFu's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://www.pickfu.com/docs/api-reference
- **OpenAPI specification:** https://www.pickfu.com/docs/api-reference/openapi.json
- **API base URL:** `https://api.pickfu.com/v1`

## Authentication

### API Key

Authenticate PickFu requests with a dashboard API key passed as a Bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.pickfu.com/docs/developers/authentication)

## API conventions

The total page count is read from `pagination.totalPages`. The current page number is read from `pagination.page`.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://www.pickfu.com/docs/api-reference/projects/create-project) |
| [Create Survey](actions/create-survey.md) | `POST /surveys` | [docs](https://www.pickfu.com/docs/api-reference/surveys/create-survey) |
| [Create Tag](actions/create-tag.md) | `POST /tags` | [docs](https://www.pickfu.com/docs/api-reference/tags/create-tag) |
| [Delete Survey](actions/delete-survey.md) | `DELETE /surveys/[:id]` | [docs](https://www.pickfu.com/docs/api-reference/surveys/delete-survey) |
| [Get Project](actions/get-project.md) | `GET /projects/[:id]` | [docs](https://www.pickfu.com/docs/api-reference/projects/get-project) |
| [Get Reporting Traits](actions/get-reporting-traits.md) | `GET /traits/reporting` | [docs](https://www.pickfu.com/docs/api-reference/traits/get-reporting-traits) |
| [Get Survey](actions/get-survey.md) | `GET /surveys/[:id]` | [docs](https://www.pickfu.com/docs/api-reference/surveys/get-survey) |
| [Get Survey Responses](actions/get-survey-responses.md) | `GET /surveys/[:id]/responses` | [docs](https://www.pickfu.com/docs/api-reference/responses/get-survey-responses) |
| [Get Targeting Traits](actions/get-targeting-traits.md) | `GET /traits/targeting` | [docs](https://www.pickfu.com/docs/api-reference/traits/get-targeting-traits) |
| [List Playbooks](actions/list-playbooks.md) | `GET /playbooks` | [docs](https://www.pickfu.com/docs/api-reference/playbooks/list-playbooks) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://www.pickfu.com/docs/api-reference/projects/list-projects) |
| [List Surveys](actions/list-surveys.md) | `GET /surveys` | [docs](https://www.pickfu.com/docs/api-reference/surveys/list-surveys) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://www.pickfu.com/docs/api-reference/tags/list-tags) |
| [Search Help Articles](actions/search-help-articles.md) | `GET /help/search` | [docs](https://www.pickfu.com/docs/api-reference/help/search-help-articles) |
| [Update Project](actions/update-project.md) | `PATCH /projects/[:id]` | [docs](https://www.pickfu.com/docs/api-reference/projects/update-project) |
| [Update Survey](actions/update-survey.md) | `PATCH /surveys/[:id]` | [docs](https://www.pickfu.com/docs/api-reference/surveys/update-survey) |
