# Timelink: Native API Reference

A consolidated summary of Timelink's API configuration and 39 documented operations, with links to official documentation.

- **Official docs:** https://api.timelink.io/documentation
- **OpenAPI specification:** https://api.timelink.io/docs?api-docs.json
- **API base URL:** `https://api.timelink.io/api/v1`

## Authentication

### API Token

Authenticate with a Timelink API token. MindCloud sends the token as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.timelink.io/api)

## API conventions

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 100; minimum 1).

## Endpoints (39 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | `POST /clients` | [docs](https://api.timelink.io/documentation#/Clients/post_api_v1_clients) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://api.timelink.io/documentation#/Projects/post_api_v1_projects) |
| [Create Service](actions/create-service.md) | `POST /services` | [docs](https://api.timelink.io/documentation#/Services/post_api_v1_services) |
| [Create Time Entry](actions/create-time-entry.md) | `POST /timeEntries` | [docs](https://api.timelink.io/documentation#/Time%20Entries/post_api_v1_timeEntries) |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://api.timelink.io/documentation#/Users/post_api_v1_users) |
| [Delete Client](actions/delete-client.md) | `DELETE /clients/:id` | [docs](https://api.timelink.io/documentation#/Clients/delete_api_v1_clients__id_) |
| [Delete Client by External ID](actions/delete-client-by-external-id.md) | `DELETE /clients/ext/:extId` | [docs](https://api.timelink.io/documentation#/Clients/delete_api_v1_clients_ext__ext-id_) |
| [Delete Project](actions/delete-project.md) | `DELETE /projects/:id` | [docs](https://api.timelink.io/documentation#/Projects/delete_api_v1_projects__id_) |
| [Delete Service](actions/delete-service.md) | `DELETE /services/:id` | [docs](https://api.timelink.io/documentation#/Services/delete_api_v1_services__id_) |
| [Delete Time Entry](actions/delete-time-entry.md) | `DELETE /timeEntries/:id` | [docs](https://api.timelink.io/documentation#/Time%20Entries/delete_api_v1_timeEntries__id_) |
| [Delete Time Entry by External ID](actions/delete-time-entry-by-external-id.md) | `DELETE /timeEntries/ext/:extId` | [docs](https://api.timelink.io/documentation#/Time%20Entries/delete_api_v1_timeEntries_ext__ext-id_) |
| [Export Time Entries](actions/export-time-entries.md) | `POST /timeEntries/export` | [docs](https://api.timelink.io/documentation#/Time%20Entries/post_api_v1_timeEntries_export) |
| [Get Client](actions/get-client.md) | `GET /clients/:id` | [docs](https://api.timelink.io/documentation#/Clients/get_api_v1_clients__id_) |
| [Get Company](actions/get-company.md) | `GET /company` | [docs](https://api.timelink.io/documentation#/Company/get_api_v1_company) |
| [Get Project](actions/get-project.md) | `GET /projects/:id` | [docs](https://api.timelink.io/documentation#/Projects/get_api_v1_projects__id_) |
| [Get Required Time Entry Fields](actions/get-required-time-entry-fields.md) | `GET /timeEntries/fieldsRequired` | [docs](https://api.timelink.io/documentation#/Time%20Entries/get_api_v1_timeEntries_fieldsRequired) |
| [Get Service](actions/get-service.md) | `GET /services/:id` | [docs](https://api.timelink.io/documentation#/Services/get_api_v1_services__id_) |
| [Get Time Entry](actions/get-time-entry.md) | `GET /timeEntries/:id` | [docs](https://api.timelink.io/documentation#/Time%20Entries/get_api_v1_timeEntries__id_) |
| [Get Time Entry by External ID](actions/get-time-entry-by-external-id.md) | `GET /timeEntries/ext/:extId` | [docs](https://api.timelink.io/documentation#/Time%20Entries/get_api_v1_timeEntries_ext__ext-id_) |
| [Get User](actions/get-user.md) | `GET /users/:id` | [docs](https://api.timelink.io/documentation#/Users/get_api_v1_users__id_) |
| [List Active Time Entries](actions/list-active-time-entries.md) | `GET /timeEntries/active` | [docs](https://api.timelink.io/documentation#/Time%20Entries/get_api_v1_timeEntries_active) |
| [List Clients](actions/list-clients.md) | `GET /clients` | [docs](https://api.timelink.io/documentation#/Clients/get_api_v1_clients) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://api.timelink.io/documentation#/Projects/get_api_v1_projects) |
| [List Services](actions/list-services.md) | `GET /services` | [docs](https://api.timelink.io/documentation#/Services/get_api_v1_services) |
| [List Time Entries](actions/list-time-entries.md) | `GET /timeEntries` | [docs](https://api.timelink.io/documentation#/Time%20Entries/get_api_v1_timeEntries) |
| [List Time Entry Conflicts](actions/list-time-entry-conflicts.md) | `GET /timeEntries/conflicts` | [docs](https://api.timelink.io/documentation#/Time%20Entries/get_api_v1_timeEntries_conflicts) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://api.timelink.io/documentation#/Users/get_api_v1_users) |
| [Search Clients](actions/search-clients.md) | `POST /clients/search` | [docs](https://api.timelink.io/documentation#/Clients/post_api_v1_clients_search) |
| [Search Projects](actions/search-projects.md) | `POST /projects/search` | [docs](https://api.timelink.io/documentation#/Projects/post_api_v1_projects_search) |
| [Search Services](actions/search-services.md) | `POST /services/search` | [docs](https://api.timelink.io/documentation#/Services/post_api_v1_services_search) |
| [Search Time Entries](actions/search-time-entries.md) | `POST /timeEntries/search` | [docs](https://api.timelink.io/documentation#/Time%20Entries/post_api_v1_timeEntries_search) |
| [Update Client](actions/update-client.md) | `PATCH /clients/:id` | [docs](https://api.timelink.io/documentation#/Clients/patch_api_v1_clients__id_) |
| [Update Client by External ID](actions/update-client-by-external-id.md) | `PATCH /clients/ext/:extId` | [docs](https://api.timelink.io/documentation#/Clients/patch_api_v1_clients_ext__ext-id_) |
| [Update Company Settings](actions/update-company-settings.md) | `PATCH /company/settings` | [docs](https://api.timelink.io/documentation#/Company/patch_api_v1_company_settings) |
| [Update Project](actions/update-project.md) | `PATCH /projects/:id` | [docs](https://api.timelink.io/documentation#/Projects/patch_api_v1_projects__id_) |
| [Update Project by External ID](actions/update-project-by-external-id.md) | `PATCH /projects/ext/:extId` | [docs](https://api.timelink.io/documentation#/Projects/patch_api_v1_projects_ext__ext-id_) |
| [Update Service](actions/update-service.md) | `PATCH /services/:id` | [docs](https://api.timelink.io/documentation#/Services/patch_api_v1_services__id_) |
| [Update Time Entry](actions/update-time-entry.md) | `PATCH /timeEntries/:id` | [docs](https://api.timelink.io/documentation#/Time%20Entries/patch_api_v1_timeEntries__id_) |
| [Update Time Entry by External ID](actions/update-time-entry-by-external-id.md) | `PATCH /timeEntries/ext/:extId` | [docs](https://api.timelink.io/documentation#/Time%20Entries/patch_api_v1_timeEntries_ext_ext-id_) |
