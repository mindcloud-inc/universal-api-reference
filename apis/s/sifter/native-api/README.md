# Sifter: Native API Reference

A consolidated summary of Sifter's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://sifterapp.com/developer/documentation/
- **API base URL:** `https://{subdomain}.sifterapp.com/api`

## Authentication

### API Key

Connect with a Sifter access key and account subdomain.

### Credentials

- **API Key:** `apiKey` · required
- **Account Subdomain:** `subdomain` · required · Your Sifter account subdomain, without .sifterapp.com.

Send these headers with each API request:

```http
X-Sifter-Token: <apiKey>
```

[Official authentication documentation](https://sifterapp.com/developer/overview/)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON. The total page count is read from `total_pages`. The current page number is read from `page`.

## Pagination

Use `per_page` in the query string to set the page size (default 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | `POST /projects/:project_id/issues/:issue_id` | [docs](https://sifterapp.com/developer/documentation/comments/) |
| [Create Issue](actions/create-issue.md) | `POST /projects/:project_id/issues` | [docs](https://sifterapp.com/developer/documentation/issues/) |
| [Get Issue](actions/get-issue.md) | `GET /projects/:project_id/issues/:issue_id` | [docs](https://sifterapp.com/developer/documentation/issues/) |
| [Get Project](actions/get-project.md) | `GET /projects/:project_id` | [docs](https://sifterapp.com/developer/documentation/projects/) |
| [Get Project Metadata](actions/get-project-metadata.md) | `GET /projects/:project_id` | [docs](https://sifterapp.com/developer/documentation/projects/) |
| [List All Projects](actions/list-all-projects.md) | `GET /projects` | [docs](https://sifterapp.com/developer/documentation/projects/) |
| [List Issues](actions/list-issues.md) | `GET /projects/:project_id/issues` | [docs](https://sifterapp.com/developer/documentation/issues/) |
| [List Priorities](actions/list-priorities.md) | `GET /priorities` | [docs](https://sifterapp.com/developer/documentation/priorities/) |
| [List Project Categories](actions/list-project-categories.md) | `GET /projects/:project_id/categories` | [docs](https://sifterapp.com/developer/documentation/projects/) |
| [List Project Milestones](actions/list-project-milestones.md) | `GET /projects/:project_id/milestones` | [docs](https://sifterapp.com/developer/documentation/projects/) |
| [List Project People](actions/list-project-people.md) | `GET /projects/:project_id/people` | [docs](https://sifterapp.com/developer/documentation/projects/) |
| [List Project Statuses](actions/list-project-statuses.md) | `GET /projects/:project_id/statuses` | [docs](https://sifterapp.com/developer/documentation/statuses/) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://sifterapp.com/developer/documentation/projects/) |
| [Update Issue](actions/update-issue.md) | `POST /projects/:project_id/issues/:issue_id` | [docs](https://sifterapp.com/developer/documentation/comments/) |
