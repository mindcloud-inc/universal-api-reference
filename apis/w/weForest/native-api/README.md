# WeForest: Native API Reference

A consolidated summary of WeForest's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.weforest.org
- **API base URL:** `https://api.weforest.org`

## Authentication

### API Key

Authenticate WeForest API requests with an API key from the WeForest dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.weforest.org/authentication)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add item(s) to tree-planting order](actions/add-item-s-to-tree-planting-order.md) | `POST /trees/:id/items` | [docs](https://docs.weforest.org/add-item-s-to-tree-planting-order) |
| [Create a donation form checkout session](actions/create-a-donation-form-checkout-session.md) | `POST /forms/:id/checkout` | [docs](https://docs.weforest.org/create-a-donation-form-checkout-session) |
| [Create a new user for customer](actions/create-a-new-user-for-customer.md) | `POST /customers/:id/users` | [docs](https://docs.weforest.org/create-a-new-user-for-customer) |
| [Delete order item](actions/delete-order-item.md) | `DELETE /trees/:orderId/items/:itemId` | [docs](https://docs.weforest.org/delete-order-item) |
| [Delete tree-planting request](actions/delete-tree-planting-request.md) | `DELETE /trees/:id` | [docs](https://docs.weforest.org/delete-tree-planting-request) |
| [Delete user record](actions/delete-user-record.md) | `DELETE /users/:id` | [docs](https://docs.weforest.org/delete-user-record) |
| [Get all customer users](actions/get-all-customer-users.md) | `GET /customers/:id/users` | [docs](https://docs.weforest.org/get-all-customer-users) |
| [Get all projects](actions/get-all-projects.md) | `GET /projects` | [docs](https://docs.weforest.org/get-all-projects) |
| [Get all projects customer has supported](actions/get-all-projects-customer-has-supported.md) | `GET /customers/:id/projects` | [docs](https://docs.weforest.org/get-all-projects-customer-has-supported) |
| [Get all tree-planting requests](actions/get-all-tree-planting-requests.md) | `GET /trees` | [docs](https://docs.weforest.org/get-all-tree-planting-requests) |
| [Get all trees for customer](actions/get-all-trees-for-customer.md) | `GET /customers/:id/trees` | [docs](https://docs.weforest.org/get-all-trees-for-customer) |
| [Get all users](actions/get-all-users.md) | `GET /users` | [docs](https://docs.weforest.org/get-all-users) |
| [Get authenticated user record](actions/get-authenticated-user-record.md) | `GET /whoami` | [docs](https://docs.weforest.org/get-authenticated-user-record) |
| [Get customer record](actions/get-customer-record.md) | `GET /customers/:id` | [docs](https://docs.weforest.org/get-customer-record) |
| [Get donation form](actions/get-donation-form.md) | `GET /forms/:id` | [docs](https://docs.weforest.org/get-donation-form) |
| [Get order item](actions/get-order-item.md) | `GET /trees/:orderId/items/:itemId` | [docs](https://docs.weforest.org/get-order-item) |
| [Get project](actions/get-project.md) | `GET /projects/:id` | [docs](https://docs.weforest.org/get-project) |
| [Get tree-planting request](actions/get-tree-planting-request.md) | `GET /trees/:id` | [docs](https://docs.weforest.org/get-tree-planting-request) |
| [Get user record](actions/get-user-record.md) | `GET /users/:id` | [docs](https://docs.weforest.org/get-user-record) |
| [Plant a new tree for customer](actions/plant-a-new-tree-for-customer.md) | `POST /customers/:id/trees` | [docs](https://docs.weforest.org/plant-a-new-tree-for-customer) |
| [Plant a tree](actions/plant-a-tree.md) | `POST /trees` | [docs](https://docs.weforest.org/plant-a-tree) |
| [Update customer record](actions/update-customer-record.md) | `PATCH /customers/:id` | [docs](https://docs.weforest.org/update-customer-record) |
| [Update order item](actions/update-order-item.md) | `PATCH /trees/:orderId/items/:itemId` | [docs](https://docs.weforest.org/update-order-item) |
| [Update user record](actions/update-user-record.md) | `PATCH /users/:id` | [docs](https://docs.weforest.org/update-user-record) |
