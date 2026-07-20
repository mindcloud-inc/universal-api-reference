# Hubflo: Native API Reference

A consolidated summary of Hubflo's API configuration and 27 documented operations, with links to official documentation.

- **Official docs:** https://hubflo.readme.io/reference/the-hubflo-api
- **API base URL:** `https://app.hubflo.com/api/v2`

## Authentication

### API Key

Use a Hubflo API key generated from the organization integrations settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://hubflo.readme.io/reference/getting-started-1)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (27 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | `POST /companies` | [docs](https://hubflo.readme.io/reference/post_api-v2-companies) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://hubflo.readme.io/reference/post_api-v2-contacts) |
| [Create Ping](actions/create-ping.md) | `POST /pings` | [docs](https://hubflo.readme.io/reference/post_api-v2-pings) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://hubflo.readme.io/reference/post_api-v2-projects) |
| [Create Proposal](actions/create-proposal.md) | `POST /proposals` | [docs](https://hubflo.readme.io/reference/post_api-v2-proposals) |
| [Create Quote Item for Proposal](actions/create-quote-item-for-proposal.md) | `POST /proposals/:proposal_id/line-items` | [docs](https://hubflo.readme.io/reference/post_api-v2-proposals-proposal-id-line-items) |
| [Create Task](actions/create-task.md) | `POST /tasks` | [docs](https://hubflo.readme.io/reference/post_api-v2-tasks) |
| [Create Workspace](actions/create-workspace.md) | `POST /workspaces` | [docs](https://hubflo.readme.io/reference/post_api-v2-workspaces) |
| [Issue Proposal](actions/issue-proposal.md) | `POST /proposals/:proposal_id/issuances` | [docs](https://hubflo.readme.io/reference/post_api-v2-proposals-proposal-id-issuances) |
| [List Companies](actions/list-companies.md) | `GET /companies` | [docs](https://hubflo.readme.io/reference/get_api-v2-companies) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://hubflo.readme.io/reference/get_api-v2-contacts) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://hubflo.readme.io/reference/get_api-v2-organizations) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://hubflo.readme.io/reference/get_api-v2-projects) |
| [List Proposals](actions/list-proposals.md) | `GET /proposals` | [docs](https://hubflo.readme.io/reference/get_api-v2-proposals) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://hubflo.readme.io/reference/get_api-v2-tasks) |
| [List Workspaces](actions/list-workspaces.md) | `GET /workspaces` | [docs](https://hubflo.readme.io/reference/get_api-v2-workspaces) |
| [Retrieve Company](actions/retrieve-company.md) | `GET /companies/:id` | [docs](https://hubflo.readme.io/reference/get_api-v2-companies-id) |
| [Retrieve Contact](actions/retrieve-contact.md) | `GET /contacts/:id` | [docs](https://hubflo.readme.io/reference/get_api-v2-contacts-id) |
| [Retrieve Project](actions/retrieve-project.md) | `GET /projects/:id` | [docs](https://hubflo.readme.io/reference/get_api-v2-projects-id) |
| [Retrieve Proposal](actions/retrieve-proposal.md) | `GET /proposals/:id` | [docs](https://hubflo.readme.io/reference/get_api-v2-proposals-id) |
| [Retrieve Task](actions/retrieve-task.md) | `GET /tasks/:id` | [docs](https://hubflo.readme.io/reference/get_api-v2-tasks-id) |
| [Retrieve Workspace](actions/retrieve-workspace.md) | `GET /workspaces/:id` | [docs](https://hubflo.readme.io/reference/get_api-v2-workspaces-id) |
| [Update Company](actions/update-company.md) | `PATCH /companies/:id` | [docs](https://hubflo.readme.io/reference/patch_api-v2-companies-id) |
| [Update Contact](actions/update-contact.md) | `PATCH /contacts/:id` | [docs](https://hubflo.readme.io/reference/patch_api-v2-contacts-id) |
| [Update Project](actions/update-project.md) | `PATCH /projects/:id` | [docs](https://hubflo.readme.io/reference/patch_api-v2-projects-id) |
| [Update Task](actions/update-task.md) | `PATCH /tasks/:id` | [docs](https://hubflo.readme.io/reference/patch_api-v2-tasks-id) |
| [Update Workspace](actions/update-workspace.md) | `PATCH /workspaces/:id` | [docs](https://hubflo.readme.io/reference/patch_api-v2-workspaces-id) |
