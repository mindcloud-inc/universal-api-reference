# Klipfolio: Native API Reference

A consolidated summary of Klipfolio's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.klipfolio.com/reference
- **API base URL:** `https://app.klipfolio.com/api/1.0`

## Authentication

### Klipfolio API Key

Connect with your Klipfolio API key. Requests send the key in the kf-api-key header.

### Credentials

- **API Key:** `apiKey` · required · Paste your Klipfolio API key. It will be sent in the kf-api-key header.

Send these headers with each API request:

```http
kf-api-key: <apiKey>
```

[Official authentication documentation](https://support.klipfolio.com/hc/en-us/articles/215548478-Klips-Generating-a-Klipfolio-API-key)

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Find Group By External ID](actions/find-group-by-external-id.md) | `GET /groups` | [docs](https://apidocs.klipfolio.com/reference/groups) |
| [Get Data Source](actions/get-data-source.md) | `GET /datasources/:datasourceId` | [docs](https://apidocs.klipfolio.com/reference/data-sources) |
| [Get Data Source Data](actions/get-data-source-data.md) | `GET /datasources/:datasourceId/data` | [docs](https://apidocs.klipfolio.com/reference/data-sources) |
| [Get Data Source Instance Data](actions/get-data-source-instance-data.md) | `GET /datasource-instances/:instanceId/data` | [docs](https://apidocs.klipfolio.com/reference/data-sources) |
| [Get Data Source Share Rights](actions/get-data-source-share-rights.md) | `GET /datasources/:datasourceId/share-rights` | [docs](https://apidocs.klipfolio.com/reference/data-sources) |
| [Get Group](actions/get-group.md) | `GET /groups/:groupId` | [docs](https://apidocs.klipfolio.com/reference/groups) |
| [Get Klip](actions/get-klip.md) | `GET /klips/:klipId` | [docs](https://apidocs.klipfolio.com/reference/klips) |
| [Get Klip Share Rights](actions/get-klip-share-rights.md) | `GET /klips/:klipId/share-rights` | [docs](https://apidocs.klipfolio.com/reference/klips) |
| [Get Profile](actions/get-profile.md) | `GET /profile` | [docs](https://apidocs.klipfolio.com/reference/profile) |
| [Get Role](actions/get-role.md) | `GET /roles/:roleId` | [docs](https://apidocs.klipfolio.com/reference/roles) |
| [Get User](actions/get-user.md) | `GET /users/:userId` | [docs](https://apidocs.klipfolio.com/reference/users) |
| [List Data Sources](actions/list-data-sources.md) | `GET /datasources` | [docs](https://apidocs.klipfolio.com/reference/data-sources) |
| [List Group Default Tabs](actions/list-group-default-tabs.md) | `GET /groups/:groupId/default-tabs` | [docs](https://apidocs.klipfolio.com/reference/groups) |
| [List Group Users](actions/list-group-users.md) | `GET /groups/:groupId/users` | [docs](https://apidocs.klipfolio.com/reference/groups) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://apidocs.klipfolio.com/reference/groups) |
| [List Klips](actions/list-klips.md) | `GET /klips` | [docs](https://apidocs.klipfolio.com/reference/klips) |
| [List Klips By Data Source](actions/list-klips-by-data-source.md) | `GET /klips` | [docs](https://apidocs.klipfolio.com/reference/klips) |
| [List Role Permissions](actions/list-role-permissions.md) | `GET /roles/:roleId/permissions` | [docs](https://apidocs.klipfolio.com/reference/permissions) |
| [List Role Users](actions/list-role-users.md) | `GET /roles/:roleId/users` | [docs](https://apidocs.klipfolio.com/reference/roles) |
| [List Roles](actions/list-roles.md) | `GET /roles` | [docs](https://apidocs.klipfolio.com/reference/roles) |
| [List Tabs](actions/list-tabs.md) | `GET /tabs` | [docs](https://apidocs.klipfolio.com/reference/tabs-now-called-dashboards) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://apidocs.klipfolio.com/reference) |
| [List User Groups](actions/list-user-groups.md) | `GET /users/:userId/groups` | [docs](https://apidocs.klipfolio.com/reference/groups) |
| [List User Roles](actions/list-user-roles.md) | `GET /users/:userId/roles` | [docs](https://apidocs.klipfolio.com/reference/user-roles) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://apidocs.klipfolio.com/reference/users) |
