# Productlane: Native API Reference

A consolidated summary of Productlane's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://productlane.com/docs/integrations/api
- **API base URL:** `https://productlane.com/api/v1`

## Authentication

### API key

Authenticate with a Productlane API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://productlane.mintlify.dev/docs/api/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `take` in the query string to set the page size. Use `skip` in the query string as the record offset; numbering starts at 0.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Changelog](actions/create-changelog.md) | `POST /changelogs` | [docs](https://productlane.mintlify.dev/docs/api/changelogs/create-changelog) |
| [Create Company](actions/create-company.md) | `POST /companies` | [docs](https://productlane.mintlify.dev/docs/api/companies/create-company) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://productlane.mintlify.dev/docs/api/contacts/create-contact) |
| [Create Doc Article](actions/create-doc-article.md) | `POST /docs/articles` | [docs](https://productlane.mintlify.dev/docs/api/docs/create-doc-article) |
| [Create Doc Group](actions/create-doc-group.md) | `POST /docs/groups` | [docs](https://productlane.mintlify.dev/docs/api/docs/create-doc-group) |
| [Create Thread](actions/create-thread.md) | `POST /threads` | [docs](https://productlane.mintlify.dev/docs/api/threads/create-thread) |
| [Delete Changelog](actions/delete-changelog.md) | `DELETE /changelogs/:id` | [docs](https://productlane.mintlify.dev/docs/api/changelogs/delete-changelog) |
| [Delete Company](actions/delete-company.md) | `DELETE /companies/:id` | [docs](https://productlane.mintlify.dev/docs/api/companies/delete-company) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:id` | [docs](https://productlane.mintlify.dev/docs/api/contacts/delete-contact) |
| [Delete Doc Article](actions/delete-doc-article.md) | `DELETE /docs/articles/{id}` | [docs](https://productlane.mintlify.dev/docs/api/docs/delete-doc-article) |
| [Delete Doc Group](actions/delete-doc-group.md) | `DELETE /docs/groups/{id}` | [docs](https://productlane.mintlify.dev/docs/api/docs/delete-doc-group) |
| [Get Changelog](actions/get-changelog.md) | `GET /changelogs/:workspaceId/:changelogId` | [docs](https://productlane.mintlify.dev/docs/api/changelogs/get-changelog) |
| [Get Company](actions/get-company.md) | `GET /companies/:id` | [docs](https://productlane.mintlify.dev/docs/api/companies/get-company) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id` | [docs](https://productlane.mintlify.dev/docs/api/contacts/get-contact) |
| [Get Doc Article](actions/get-doc-article.md) | `GET /docs/articles/{workspaceId}/{articleId}` | [docs](https://productlane.mintlify.dev/docs/api/docs/get-doc-article) |
| [Get Issue](actions/get-issue.md) | `GET /issues/{workspaceId}/{issueId}` | [docs](https://productlane.mintlify.dev/docs/api/portal/get-issue) |
| [Get Project](actions/get-project.md) | `GET /projects/{workspaceId}/{projectId}` | [docs](https://productlane.mintlify.dev/docs/api/portal/get-project) |
| [Get Thread](actions/get-thread.md) | `GET /threads/:id` | [docs](https://productlane.mintlify.dev/docs/api/threads/get-thread) |
| [Get Upvotes](actions/get-upvotes.md) | `GET /portal/upvotes` | [docs](https://productlane.mintlify.dev/docs/api/portal/get-upvotes) |
| [Get Workspace](actions/get-workspace.md) | `GET /workspaces/{id}` | [docs](https://productlane.mintlify.dev/docs/api/workspaces/get-workspace) |
| [Invite User](actions/invite-user.md) | `POST /users/invite` | [docs](https://productlane.mintlify.dev/docs/api/users/invite-user) |
| [List Changelog Tags](actions/list-changelog-tags.md) | `GET /changelog-tags/:workspaceId` | [docs](https://productlane.mintlify.dev/docs/api/changelogs/list-changelog-tags) |
| [List Changelogs](actions/list-changelogs.md) | `GET /changelogs/:workspaceId` | [docs](https://productlane.mintlify.dev/docs/api/changelogs/list-changelogs) |
| [List Companies](actions/list-companies.md) | `GET /companies` | [docs](https://productlane.mintlify.dev/docs/api/companies/list-companies) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://productlane.mintlify.dev/docs/api/contacts/get-contacts) |
| [List Doc Articles](actions/list-doc-articles.md) | `GET /docs/articles/{workspaceId}` | [docs](https://productlane.mintlify.dev/docs/api/docs/list-doc-articles) |
| [List Issues](actions/list-issues.md) | `GET /issues/{workspaceId}` | [docs](https://productlane.mintlify.dev/docs/api/portal/list-issues) |
| [List Members](actions/list-members.md) | `GET /users` | [docs](https://productlane.mintlify.dev/docs/api/users/list-members) |
| [List Projects](actions/list-projects.md) | `GET /projects/{workspaceId}` | [docs](https://productlane.mintlify.dev/docs/api/portal/list-projects) |
| [List Threads](actions/list-threads.md) | `GET /threads` | [docs](https://productlane.mintlify.dev/docs/api/threads/list-threads) |
| [Move Articles To Group](actions/move-articles-to-group.md) | `POST /docs/groups/move-articles` | [docs](https://productlane.mintlify.dev/docs/api/docs/move-articles-to-group) |
| [Send Message](actions/send-message.md) | `POST /threads/:threadId/messages` | [docs](https://productlane.mintlify.dev/docs/api/threads/send-message) |
| [Update Changelog](actions/update-changelog.md) | `PATCH /changelogs/:id` | [docs](https://productlane.mintlify.dev/docs/api/changelogs/update-changelog) |
| [Update Company](actions/update-company.md) | `PATCH /companies/:id` | [docs](https://productlane.mintlify.dev/docs/api/companies/update-company) |
| [Update Contact](actions/update-contact.md) | `PATCH /contacts/:id` | [docs](https://productlane.mintlify.dev/docs/api/contacts/update-contact) |
| [Update Doc Article](actions/update-doc-article.md) | `PATCH /docs/articles/{id}` | [docs](https://productlane.mintlify.dev/docs/api/docs/update-doc-article) |
| [Update Doc Group](actions/update-doc-group.md) | `PATCH /docs/groups/{id}` | [docs](https://productlane.mintlify.dev/docs/api/docs/update-doc-group) |
| [Update Thread](actions/update-thread.md) | `PATCH /threads/:id` | [docs](https://productlane.mintlify.dev/docs/api/threads/update-thread) |
| [Update User Role](actions/update-user-role.md) | `PATCH /users/role` | [docs](https://productlane.mintlify.dev/docs/api/users/update-user-role) |
| [Upvote Project](actions/upvote-project.md) | `POST /portal/upvotes` | [docs](https://productlane.mintlify.dev/docs/api/portal/upvote-project) |
