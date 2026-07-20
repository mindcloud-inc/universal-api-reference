# Rocketadmin: Native API Reference

A consolidated summary of Rocketadmin's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.rocketadmin.com/api-reference/rocketadmin
- **API base URL:** `https://app.rocketadmin.com/api`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.rocketadmin.com/api-reference/api-key-controller-check-api-key)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Table Row](actions/add-table-row.md) | `POST /table/row/:connectionId` | [docs](https://docs.rocketadmin.com/api-reference/table-controller-add-row-in-table) |
| [Check API Key](actions/check-api-key.md) | `GET /check/apikey` | [docs](https://docs.rocketadmin.com/api-reference/api-key-controller-check-api-key) |
| [Create API Key](actions/create-api-key.md) | `POST /apikey` | [docs](https://docs.rocketadmin.com/api-reference/api-key-controller-create-api-key) |
| [Delete API Key](actions/delete-api-key.md) | `DELETE /apikey/:apiKeyId` | [docs](https://docs.rocketadmin.com/api-reference/api-key-controller-delete-api-key) |
| [Delete Table Row](actions/delete-table-row.md) | `DELETE /table/row/:connectionId` | [docs](https://docs.rocketadmin.com/api-reference/table-controller-delete-row-in-table) |
| [Delete Table Rows](actions/delete-table-rows.md) | `PUT /table/rows/delete/:connectionId` | [docs](https://docs.rocketadmin.com/api-reference/table-controller-delete-rows-in-table) |
| [Get API Key](actions/get-api-key.md) | `GET /apikey/:apiKeyId` | [docs](https://docs.rocketadmin.com/api-reference/api-key-controller-get-api-key) |
| [Get Connection](actions/get-connection.md) | `GET /connection/one/:connectionId` | [docs](https://docs.rocketadmin.com/api-reference/connection-controller-find-one) |
| [Get Connection Properties](actions/get-connection-properties.md) | `GET /connection/properties/:connectionId` | [docs](https://docs.rocketadmin.com/api-reference/connection-properties-controller-find-connection-properties) |
| [Get Current Company](actions/get-current-company.md) | `GET /company/my` | [docs](https://docs.rocketadmin.com/api-reference/company-info-controller-get-user-company) |
| [Get Current Company Full Info](actions/get-current-company-full-info.md) | `GET /company/my/full` | [docs](https://docs.rocketadmin.com/api-reference/company-info-controller-get-user-companies) |
| [Get Current User](actions/get-current-user.md) | `GET /user` | [docs](https://docs.rocketadmin.com/api-reference/user-controller-find-me) |
| [Get Table Filter](actions/get-table-filter.md) | `GET /table-filters/:connectionId/:filterId` | [docs](https://docs.rocketadmin.com/api-reference/table-filters-controller-find-table-filter-by-id) |
| [Get Table Row By Primary Key](actions/get-table-row-by-primary-key.md) | `GET /table/row/:connectionId` | [docs](https://docs.rocketadmin.com/api-reference/table-controller-get-row-by-primary-key) |
| [Get Table Structure](actions/get-table-structure.md) | `GET /table/structure/:connectionId` | [docs](https://docs.rocketadmin.com/api-reference/table-controller-get-table-structure) |
| [Get User Session Settings](actions/get-user-session-settings.md) | `GET /user/settings` | [docs](https://docs.rocketadmin.com/api-reference/user-controller-get-user-session-settings) |
| [List API Keys](actions/list-api-keys.md) | `GET /apikeys` | [docs](https://docs.rocketadmin.com/api-reference/api-key-controller-get-api-keys) |
| [List Company Users](actions/list-company-users.md) | `GET /company/users/:companyId` | [docs](https://docs.rocketadmin.com/api-reference/company-info-controller-get-users-in-company) |
| [List Connection Groups](actions/list-connection-groups.md) | `GET /connection/groups/:connectionId` | [docs](https://docs.rocketadmin.com/api-reference/connection-controller-get-groups-in-connection) |
| [List Connection Logs](actions/list-connection-logs.md) | `GET /logs/:connectionId` | [docs](https://docs.rocketadmin.com/api-reference/table-logs-controller-find-all) |
| [List Connection Tables](actions/list-connection-tables.md) | `GET /connection/tables/:connectionId` | [docs](https://docs.rocketadmin.com/api-reference/table-controller-find-tables-in-connection) |
| [List Connection Tables V2](actions/list-connection-tables-v2.md) | `GET /connection/tables/v2/:connectionId` | [docs](https://docs.rocketadmin.com/api-reference/table-controller-find-tables-in-connection-v-2) |
| [List Connection Users](actions/list-connection-users.md) | `GET /connection/users/:connectionId` | [docs](https://docs.rocketadmin.com/api-reference/connection-controller-find-all-users) |
| [List Connections](actions/list-connections.md) | `GET /connections` | [docs](https://docs.rocketadmin.com/api-reference/connection-controller-find-all) |
| [List Saved Queries](actions/list-saved-queries.md) | `GET /connection/:connectionId/saved-queries` | [docs](https://docs.rocketadmin.com/api-reference/saved-db-query-controller-find-all) |
| [List Table Filters](actions/list-table-filters.md) | `GET /table-filters/:connectionId/all` | [docs](https://docs.rocketadmin.com/api-reference/table-filters-controller-find-table-filters) |
| [List Table Rows](actions/list-table-rows.md) | `GET /table/rows/:connectionId` | [docs](https://docs.rocketadmin.com/api-reference/table-controller-find-all-rows) |
| [Search Table Rows](actions/search-table-rows.md) | `POST /table/rows/find/:connectionId` | [docs](https://docs.rocketadmin.com/api-reference/table-controller-find-all-rows-with-body-filter) |
| [Update Table Row](actions/update-table-row.md) | `PUT /table/row/:connectionId` | [docs](https://docs.rocketadmin.com/api-reference/table-controller-update-row-in-table) |
| [Update Table Rows](actions/update-table-rows.md) | `PUT /table/rows/update/:connectionId` | [docs](https://docs.rocketadmin.com/api-reference/table-controller-update-rows-in-table) |
