# CentralStationCRM: Native API Reference

A consolidated summary of CentralStationCRM's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://api.centralstationcrm.net/api-docs/index.html
- **OpenAPI specification:** https://api.centralstationcrm.net/api-docs/v1/swagger.json
- **API base URL:** `https://api.centralstationcrm.net`

## Authentication

### API Key

Connect with a CentralStationCRM API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-apikey: <apiKey>
```

[Official authentication documentation](https://centralstationcrm.com/api-basics)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `perpage` in the query string to set the page size (default 50; accepted range 1–250). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Connection](actions/check-connection.md) | `GET /api/check_connection` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/default/get_api_check_connection) |
| [Count Companies](actions/count-companies.md) | `GET /api/companies/count` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Company/get_api_companies_count) |
| [Count Deals](actions/count-deals.md) | `GET /api/deals/count` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Deal/get_api_deals_count) |
| [Count People](actions/count-people.md) | `GET /api/people/count` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Person/get_api_people_count) |
| [Create Company](actions/create-company.md) | `POST /api/companies` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Company/post_api_companies) |
| [Create Deal](actions/create-deal.md) | `POST /api/deals` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Deal/post_api_deals) |
| [Create Person](actions/create-person.md) | `POST /api/people` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Person/post_api_people) |
| [Create Project](actions/create-project.md) | `POST /api/projects` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Project/post_api_projects) |
| [Create Protocol](actions/create-protocol.md) | `POST /api/protocols` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Protocol/post_api_protocols) |
| [Create Task](actions/create-task.md) | `POST /api/tasks` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Task/post_api_tasks) |
| [Delete Company](actions/delete-company.md) | `DELETE /api/companies/:id` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Company/delete_api_companies__id_) |
| [Delete Person](actions/delete-person.md) | `DELETE /api/people/:id` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Person/delete_api_people__id_) |
| [Delete Task](actions/delete-task.md) | `DELETE /api/tasks/:id` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Task/delete_api_tasks__id_) |
| [Get Company](actions/get-company.md) | `GET /api/companies/:id` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Company/get_api_companies__id_) |
| [Get Current User](actions/get-current-user.md) | `GET /api/user` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/default/get_api_user) |
| [Get Deal](actions/get-deal.md) | `GET /api/deals/:id` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Deal/get_api_deals__id_) |
| [Get Person](actions/get-person.md) | `GET /api/people/:id` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Person/get_api_people__id_) |
| [Get Project](actions/get-project.md) | `GET /api/projects/:id` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Project/get_api_projects__id_) |
| [Get Protocol](actions/get-protocol.md) | `GET /api/protocols/:id` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Protocol/get_api_protocols__id_) |
| [Get Task](actions/get-task.md) | `GET /api/tasks/:id` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Task/get_api_tasks__id_) |
| [Get User](actions/get-user.md) | `GET /api/users/:id` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/User/get_api_users__id_) |
| [List Companies](actions/list-companies.md) | `GET /api/companies` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Company/get_api_companies) |
| [List Deals](actions/list-deals.md) | `GET /api/deals` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Deal/get_api_deals) |
| [List People](actions/list-people.md) | `GET /api/people` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Person/get_api_people) |
| [List Projects](actions/list-projects.md) | `GET /api/projects` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Project/get_api_projects) |
| [List Protocols](actions/list-protocols.md) | `GET /api/protocols` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Protocol/get_api_protocols) |
| [List Tasks](actions/list-tasks.md) | `GET /api/tasks` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Task/get_api_tasks) |
| [List Users](actions/list-users.md) | `GET /api/users` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/User/get_api_users) |
| [Merge Companies](actions/merge-companies.md) | `POST /api/companies/:id/merge` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Company/post_api_companies__id__merge) |
| [Merge People](actions/merge-people.md) | `POST /api/people/:id/merge` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Person/post_api_people__id__merge) |
| [Search Companies](actions/search-companies.md) | `GET /api/companies/search` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Company/get_api_companies_search) |
| [Search Deals](actions/search-deals.md) | `GET /api/deals/search` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Deal/get_api_deals_search) |
| [Search People](actions/search-people.md) | `GET /api/people/search` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Person/get_api_people_search) |
| [Search Records](actions/search-records.md) | `GET /api/search` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Search/get_api_search) |
| [Search Users](actions/search-users.md) | `GET /api/users/search` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/User/get_api_users_search) |
| [Update Company](actions/update-company.md) | `PUT /api/companies/:id` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Company/put_api_companies__id_) |
| [Update Deal](actions/update-deal.md) | `PUT /api/deals/:id` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Deal/put_api_deals__id_) |
| [Update Person](actions/update-person.md) | `PUT /api/people/:id` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Person/put_api_people__id_) |
| [Update Project](actions/update-project.md) | `PUT /api/projects/:id` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Project/put_api_projects__id_) |
| [Update Task](actions/update-task.md) | `PUT /api/tasks/:id` | [docs](https://api.centralstationcrm.net/api-docs/index.html#/Task/put_api_tasks__id_) |
