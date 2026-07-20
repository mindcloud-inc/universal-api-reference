# Yeeflow: Native API Reference

A consolidated summary of Yeeflow's API configuration and 41 documented operations, with links to official documentation.

- **Official docs:** https://developer.yeeflow.com/api/
- **OpenAPI specification:** https://cdn.yungalaxy.com/yeeflow/developer/v1/yeeflow_en.yaml
- **API base URL:** `https://api.yeeflow.com/v1`

## Authentication

### Yeeflow API Key

Use your Yeeflow API key. The key is sent only in the apiKey request header.

### Credentials

- **API Key:** `apiKey` · optional · Your Yeeflow API key.

Send these headers with each API request:

```http
apiKey: <apiKey>
```

[Official authentication documentation](https://developer.yeeflow.com/api/)

## API conventions

Responses from this API use JSON. Response data is read from `Data`.

## Pagination

Use `pageSize` in the query string to set the page size (default 50; accepted range 1–200). Use `pageIndex` in the query string to choose the page; numbering starts at 1.

## Endpoints (41 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Users To Group](actions/add-users-to-group.md) | `POST /groups/:id/users` | [docs](https://developer.yeeflow.com/api/#tag/Groups/paths/~1groups~1{id}~1users/post) |
| [Assign Users To Position](actions/assign-users-to-position.md) | `POST /positions/:id/users` | [docs](https://developer.yeeflow.com/api/#tag/Positions/paths/~1positions~1{id}~1users/post) |
| [Create Delegation](actions/create-delegation.md) | `POST /workflow/delegates` | [docs](https://developer.yeeflow.com/api/#tag/Workflows/paths/~1workflow~1delegates/post) |
| [Create Department](actions/create-department.md) | `POST /departments` | [docs](https://developer.yeeflow.com/api/#tag/Departments/paths/~1departments/post) |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://developer.yeeflow.com/api/#tag/Groups/paths/~1groups/post) |
| [Create Location](actions/create-location.md) | `POST /locations` | [docs](https://developer.yeeflow.com/api/#tag/Locations/paths/~1locations/post) |
| [Create Position](actions/create-position.md) | `POST /positions` | [docs](https://developer.yeeflow.com/api/#tag/Positions/paths/~1positions/post) |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://developer.yeeflow.com/api/#tag/Users/paths/~1users/post) |
| [Create Webhook](actions/create-webhook.md) | `POST /hooks` | [docs](https://developer.yeeflow.com/api/#tag/Webhooks/paths/~1hooks/post) |
| [Delete Delegation](actions/delete-delegation.md) | `DELETE /workflow/delegates/:id` | [docs](https://developer.yeeflow.com/api/#tag/Workflows/paths/~1workflow~1delegates~1{id}/delete) |
| [Delete Department](actions/delete-department.md) | `DELETE /departments/:id` | [docs](https://developer.yeeflow.com/api/#tag/Departments/paths/~1departments~1{id}/delete) |
| [Delete Group](actions/delete-group.md) | `DELETE /groups/:id` | [docs](https://developer.yeeflow.com/api/#tag/Groups/paths/~1groups~1{id}/delete) |
| [Delete Location](actions/delete-location.md) | `DELETE /locations/:id` | [docs](https://developer.yeeflow.com/api/#tag/Locations/paths/~1locations~1{id}/delete) |
| [Delete Position](actions/delete-position.md) | `DELETE /positions/:id` | [docs](https://developer.yeeflow.com/api/#tag/Positions/paths/~1positions~1{id}/delete) |
| [Delete User](actions/delete-user.md) | `DELETE /users/:id` | [docs](https://developer.yeeflow.com/api/#tag/Users/paths/~1users~1{id}/delete) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /hooks/:id` | [docs](https://developer.yeeflow.com/api/#tag/Webhooks/paths/~1hooks~1{id}/delete) |
| [Disable Delegation](actions/disable-delegation.md) | `PUT /workflow/delegates/:id/disable` | [docs](https://developer.yeeflow.com/api/#tag/Workflows/paths/~1workflow~1delegates~1{id}~1disable/put) |
| [Disable User](actions/disable-user.md) | `PUT /users/:id/disable` | [docs](https://developer.yeeflow.com/api/#tag/Users/paths/~1users~1{id}~1disable/put) |
| [Enable Delegation](actions/enable-delegation.md) | `PUT /workflow/delegates/:id/enable` | [docs](https://developer.yeeflow.com/api/#tag/Workflows/paths/~1workflow~1delegates~1{id}~1enable/put) |
| [Enable User](actions/enable-user.md) | `PUT /users/:id/enable` | [docs](https://developer.yeeflow.com/api/#tag/Users/paths/~1users~1{id}~1enable/put) |
| [Get Delegation](actions/get-delegation.md) | `GET /workflow/delegates/:id` | [docs](https://developer.yeeflow.com/api/#tag/Workflows/paths/~1workflow~1delegates~1{id}/get) |
| [Get Location](actions/get-location.md) | `GET /locations/:id` | [docs](https://developer.yeeflow.com/api/#tag/Locations/paths/~1locations~1{id}/get) |
| [Get Position Assignments](actions/get-position-assignments.md) | `GET /positions/:id/users` | [docs](https://developer.yeeflow.com/api/#tag/Positions/paths/~1positions~1{id}~1users/get) |
| [Get User](actions/get-user.md) | `GET /users/:id` | [docs](https://developer.yeeflow.com/api/#tag/Users/paths/~1users~1{id}/get) |
| [Get User By Account ID](actions/get-user-by-account-id.md) | `GET /users` | [docs](https://developer.yeeflow.com/api/#tag/Users/paths/~1users/get) |
| [Get Webhook](actions/get-webhook.md) | `GET /hooks/:id` | [docs](https://developer.yeeflow.com/api/#tag/Webhooks/paths/~1hooks~1{id}/get) |
| [List Delegations](actions/list-delegations.md) | `GET /workflow/delegates` | [docs](https://developer.yeeflow.com/api/#tag/Workflows/paths/~1workflow~1delegates/get) |
| [List Departments](actions/list-departments.md) | `GET /departments` | [docs](https://developer.yeeflow.com/api/#tag/Departments/paths/~1departments/get) |
| [List Group Users](actions/list-group-users.md) | `GET /groups/:id/users` | [docs](https://developer.yeeflow.com/api/#tag/Groups/paths/~1groups~1{id}~1users/get) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://developer.yeeflow.com/api/#tag/Groups/paths/~1groups/get) |
| [List Locations](actions/list-locations.md) | `GET /locations` | [docs](https://developer.yeeflow.com/api/#tag/Locations/paths/~1locations/get) |
| [List Pending Tasks](actions/list-pending-tasks.md) | `GET /workflow/tasks/todo` | [docs](https://developer.yeeflow.com/api/#tag/Workflows/paths/~1workflow~1tasks~1todo/get) |
| [List Positions](actions/list-positions.md) | `GET /positions` | [docs](https://developer.yeeflow.com/api/#tag/Positions/paths/~1positions/get) |
| [Remove Users From Group](actions/remove-users-from-group.md) | `POST /groups/:id/users/remove` | [docs](https://developer.yeeflow.com/api/#tag/Groups/paths/~1groups~1{id}~1users~1remove/post) |
| [Remove Users From Position](actions/remove-users-from-position.md) | `POST /positions/:id/users/remove` | [docs](https://developer.yeeflow.com/api/#tag/Positions/paths/~1positions~1{id}~1users~1remove/post) |
| [Search Users](actions/search-users.md) | `POST /users/search` | [docs](https://developer.yeeflow.com/api/#tag/Users/paths/~1users~1search/post) |
| [Update Delegation](actions/update-delegation.md) | `PUT /workflow/delegates/:id` | [docs](https://developer.yeeflow.com/api/#tag/Workflows/paths/~1workflow~1delegates~1{id}/put) |
| [Update Group](actions/update-group.md) | `PUT /groups/:id` | [docs](https://developer.yeeflow.com/api/#tag/Groups/paths/~1groups~1{id}/put) |
| [Update Location](actions/update-location.md) | `PUT /locations/:id` | [docs](https://developer.yeeflow.com/api/#tag/Locations/paths/~1locations~1{id}/put) |
| [Update Position](actions/update-position.md) | `PUT /positions/:id` | [docs](https://developer.yeeflow.com/api/#tag/Positions/paths/~1positions~1{id}/put) |
| [Update User](actions/update-user.md) | `PUT /users/:id` | [docs](https://developer.yeeflow.com/api/#tag/Users/paths/~1users~1{id}/put) |
