# OfficeMaps: Native API Reference

A consolidated summary of OfficeMaps's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://api.officemaps.io/docs/
- **OpenAPI specification:** https://api.officemaps.io/docs/v1.json
- **API base URL:** `https://api.officemaps.io`

## Authentication

### API Key

Connect OfficeMaps with an API key from Main Menu (Company Name) -> Preferences -> API Keys.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.officemaps.com/portal/en/kb/articles/using-the-officemaps-api)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Department Administrator](actions/add-department-administrator.md) | `PUT /v1/department/:departmentId/administrator/:personId` | [docs](https://api.officemaps.io/docs/) |
| [Add Department Manager](actions/add-department-manager.md) | `PUT /v1/department/:departmentId/manager/:personId` | [docs](https://api.officemaps.io/docs/) |
| [Add Department Member](actions/add-department-member.md) | `PUT /v1/department/:departmentId/member/:personId` | [docs](https://api.officemaps.io/docs/) |
| [Bulk Add Department Administrators](actions/bulk-add-department-administrators.md) | `PUT /v1/department/:departmentId/administrators` | [docs](https://api.officemaps.io/docs/) |
| [Bulk Add Department Managers](actions/bulk-add-department-managers.md) | `PUT /v1/department/:departmentId/managers` | [docs](https://api.officemaps.io/docs/) |
| [Bulk Add Department Members](actions/bulk-add-department-members.md) | `PUT /v1/department/:departmentId/members` | [docs](https://api.officemaps.io/docs/) |
| [Bulk Remove Department Administrators](actions/bulk-remove-department-administrators.md) | `DELETE /v1/department/:departmentId/administrators` | [docs](https://api.officemaps.io/docs/) |
| [Bulk Remove Department Managers](actions/bulk-remove-department-managers.md) | `DELETE /v1/department/:departmentId/managers` | [docs](https://api.officemaps.io/docs/) |
| [Bulk Remove Department Members](actions/bulk-remove-department-members.md) | `DELETE /v1/department/:departmentId/members` | [docs](https://api.officemaps.io/docs/) |
| [Create Person](actions/create-person.md) | `POST /v1/person` | [docs](https://api.officemaps.io/docs/) |
| [Delete Person](actions/delete-person.md) | `DELETE /v1/person/:id` | [docs](https://api.officemaps.io/docs/) |
| [Get Department Administrators](actions/get-department-administrators.md) | `GET /v1/department/:departmentId/administrators` | [docs](https://api.officemaps.io/docs/) |
| [Get Department Details](actions/get-department-details.md) | `GET /v1/department/:departmentId` | [docs](https://api.officemaps.io/docs/) |
| [Get Department Managers](actions/get-department-managers.md) | `GET /v1/department/:departmentId/managers` | [docs](https://api.officemaps.io/docs/) |
| [Get Department Members](actions/get-department-members.md) | `GET /v1/department/:departmentId/members` | [docs](https://api.officemaps.io/docs/) |
| [Get Department Tree List](actions/get-department-tree-list.md) | `GET /v1/department/treelist` | [docs](https://api.officemaps.io/docs/) |
| [Get Department Tree List By Id](actions/get-department-tree-list-by-id.md) | `GET /v1/department/treelist/:id` | [docs](https://api.officemaps.io/docs/) |
| [Get Departments](actions/get-departments.md) | `GET /v1/department` | [docs](https://api.officemaps.io/docs/) |
| [Get Person](actions/get-person.md) | `GET /v1/person/:personId` | [docs](https://api.officemaps.io/docs/) |
| [Remove Department Administrator](actions/remove-department-administrator.md) | `DELETE /v1/department/:departmentId/administrator/:personId` | [docs](https://api.officemaps.io/docs/) |
| [Remove Department Manager](actions/remove-department-manager.md) | `DELETE /v1/department/:departmentId/manager/:personId` | [docs](https://api.officemaps.io/docs/) |
| [Remove Department Member](actions/remove-department-member.md) | `DELETE /v1/department/:departmentId/member/:personId` | [docs](https://api.officemaps.io/docs/) |
| [Search Persons](actions/search-persons.md) | `GET /v1/person` | [docs](https://api.officemaps.io/docs/) |
| [Update Person](actions/update-person.md) | `PUT /v1/person/:id` | [docs](https://api.officemaps.io/docs/) |
