# Nucleus One: Native API Reference

A consolidated summary of Nucleus One's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://client-api.nucleus.one/api/v1/docs
- **OpenAPI specification:** https://client-api.nucleus.one/api/v1/openapi.yaml
- **API base URL:** `https://client-api.nucleus.one/api/v1`

## Authentication

### API Key

Use a Nucleus One API key sent as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.ademero.com/developers/api-keys)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Organization Membership Package](actions/get-organization-membership-package.md) | `GET /organizationMembershipPackages/:organizationId` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [Get Organization Permissions](actions/get-organization-permissions.md) | `GET /organizations/:organizationId/permissions` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [Get Project](actions/get-project.md) | `GET /organizations/:organizationId/projects/:projectId` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [Get Project Settings](actions/get-project-settings.md) | `GET /organizations/:organizationId/projects/:projectId/settings` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [Get Task Stats](actions/get-task-stats.md) | `GET /organizations/:organizationId/projects/:projectId/taskStats` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [Get User Profile](actions/get-user-profile.md) | `GET /user/profile` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [List Approvals](actions/list-approvals.md) | `GET /organizations/:organizationId/projects/:projectId/approvals` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [List Completed Tasks](actions/list-completed-tasks.md) | `GET /organizations/:organizationId/projects/:projectId/completedTasks` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [List Denied Tasks](actions/list-denied-tasks.md) | `GET /organizations/:organizationId/projects/:projectId/deniedTasks` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [List Document Filter Sort Fields](actions/list-document-filter-sort-fields.md) | `GET /organizations/:organizationId/projects/:projectId/documentFilterSortFields` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [List Document Folders](actions/list-document-folders.md) | `GET /organizations/:organizationId/projects/:projectId/documentFolders` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [List Document Subscriptions](actions/list-document-subscriptions.md) | `GET /organizations/:organizationId/projects/:projectId/documentSubscriptions` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [List Documents](actions/list-documents.md) | `GET /organizations/:organizationId/projects/:projectId/documents` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [List Fields](actions/list-fields.md) | `GET /organizations/:organizationId/projects/:projectId/fields` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [List Form Templates](actions/list-form-templates.md) | `GET /organizations/:organizationId/projects/:projectId/formTemplates` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [List Groups](actions/list-groups.md) | `GET /organizations/:organizationId/projects/:projectId/groups` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [List Processes](actions/list-processes.md) | `GET /organizations/:organizationId/projects/:projectId/processes` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [List Project Comments](actions/list-project-comments.md) | `GET /organizations/:organizationId/projects/:projectId/comments` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [List Project Members](actions/list-project-members.md) | `GET /organizations/:organizationId/projects/:projectId/members` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [List Project Membership Packages](actions/list-project-membership-packages.md) | `GET /organizations/:organizationId/projectMembershipPackages` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [List Projects](actions/list-projects.md) | `GET /organizations/:organizationId/projects` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [List Recent Document Signature Forms](actions/list-recent-document-signature-forms.md) | `GET /organizations/:organizationId/projects/:projectId/recentDocumentSignatureForms` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [List Recently Accessed Documents](actions/list-recently-accessed-documents.md) | `GET /organizations/:organizationId/recentlyAccessedDocuments` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [List Recycle Bin Documents](actions/list-recycle-bin-documents.md) | `GET /organizations/:organizationId/projects/:projectId/recycleBinDocuments` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [List Tags](actions/list-tags.md) | `GET /organizations/:organizationId/projects/:projectId/tags` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [List Task Subscriptions](actions/list-task-subscriptions.md) | `GET /organizations/:organizationId/projects/:projectId/taskSubscriptions` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [List Tasks](actions/list-tasks.md) | `GET /organizations/:organizationId/projects/:projectId/tasks` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [Search Organization Content](actions/search-organization-content.md) | `GET /organizations/:organizationId/searchResults` | [docs](https://client-api.nucleus.one/api/v1/docs) |
| [Search Project Documents](actions/search-project-documents.md) | `GET /organizations/:organizationId/projects/:projectId/searchResults` | [docs](https://client-api.nucleus.one/api/v1/docs) |
