# <img src="https://images.mindcloud.co/apps/icons/images-5_1775763431407.jpeg" alt="WeForest logo" width="28" height="28"> WeForest: Universal API

WeForest API for managing users, customers, projects, trees, tree-planting orders, and donation forms.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/weForest/latest
- **Category:** Commerce
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://weforest.org
- **Vendor API docs:** https://docs.weforest.org

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get all users](actions/get-all-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weForest/latest/actions/get-all-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Checkouts

| Action | Method | Description |
| --- | --- | --- |
| [Create a donation form checkout session](actions/create-a-donation-form-checkout-session.md) | POST | Creates a donation form checkout session in WeForest. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Get customer record](actions/get-customer-record.md) | GET | Retrieves a customer record from WeForest. |
| [Update customer record](actions/update-customer-record.md) | PUT | Updates an existing customer in WeForest. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Get donation form](actions/get-donation-form.md) | GET | Retrieves a donation form from WeForest. |

### Order Lines

| Action | Method | Description |
| --- | --- | --- |
| [Add item(s) to tree-planting order](actions/add-item-s-to-tree-planting-order.md) | POST | Adds items to a tree-planting order in WeForest. |
| [Delete order item](actions/delete-order-item.md) | DELETE | Deletes an existing tree-planting order item from WeForest. |
| [Get order item](actions/get-order-item.md) | GET | Retrieves a tree-planting order item from WeForest. |
| [Update order item](actions/update-order-item.md) | PUT | Updates an existing tree-planting order item in WeForest. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Delete tree-planting request](actions/delete-tree-planting-request.md) | DELETE | Deletes an existing tree-planting request from WeForest. |
| [Get all tree-planting requests](actions/get-all-tree-planting-requests.md) | GET | Retrieves all tree-planting requests from WeForest. |
| [Get all trees for customer](actions/get-all-trees-for-customer.md) | GET | Retrieves all trees for a customer in WeForest. |
| [Get tree-planting request](actions/get-tree-planting-request.md) | GET | Retrieves a tree-planting request from WeForest. |
| [Plant a new tree for customer](actions/plant-a-new-tree-for-customer.md) | POST | Creates a new tree for a customer in WeForest. |
| [Plant a tree](actions/plant-a-tree.md) | POST | Creates a new tree-planting request in WeForest. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get all projects](actions/get-all-projects.md) | GET | Retrieves all project records from WeForest. |
| [Get all projects customer has supported](actions/get-all-projects-customer-has-supported.md) | GET | Retrieves all supported projects for a customer in WeForest. |
| [Get project](actions/get-project.md) | GET | Retrieves a project from WeForest. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create a new user for customer](actions/create-a-new-user-for-customer.md) | POST | Creates a new customer user in WeForest. |
| [Delete user record](actions/delete-user-record.md) | DELETE | Deletes an existing user from WeForest. |
| [Get all customer users](actions/get-all-customer-users.md) | GET | Retrieves all users for a customer in WeForest. |
| [Get all users](actions/get-all-users.md) | GET | Retrieves all user records from WeForest. |
| [Get authenticated user record](actions/get-authenticated-user-record.md) | GET | Retrieves the authenticated user's record from WeForest. |
| [Get user record](actions/get-user-record.md) | GET | Retrieves a user record from WeForest. |
| [Update user record](actions/update-user-record.md) | PUT | Updates an existing user in WeForest. |

