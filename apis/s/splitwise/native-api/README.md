# Splitwise: Native API Reference

A consolidated summary of Splitwise's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://dev.splitwise.com/
- **OpenAPI specification:** https://dev.splitwise.com/openapi.json
- **API base URL:** `https://secure.splitwise.com/api/v3.0`

## Authentication

### OAuth2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://secure.splitwise.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://secure.splitwise.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


[Official authentication documentation](https://dev.splitwise.com/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | `POST /create_comment` | [docs](https://dev.splitwise.com/#tag/comments/paths/~1create_comment/post) |
| [Create Expense](actions/create-expense.md) | `POST /create_expense` | [docs](https://dev.splitwise.com/#tag/expenses/paths/~1create_expense/post) |
| [Delete Comment](actions/delete-comment.md) | `POST /delete_comment/[:id]` | [docs](https://dev.splitwise.com/#tag/comments/paths/~1delete_comment~1{id}/post) |
| [Delete Expense](actions/delete-expense.md) | `POST /delete_expense/[:id]` | [docs](https://dev.splitwise.com/#tag/expenses/paths/~1delete_expense~1{id}/post) |
| [Get Current User](actions/get-current-user.md) | `GET /get_current_user` | [docs](https://dev.splitwise.com/#tag/users/paths/~1get_current_user/get) |
| [Get Expense](actions/get-expense.md) | `GET /get_expense/[:id]` | [docs](https://dev.splitwise.com/#tag/expenses/paths/~1get_expense~1{id}/get) |
| [Get Group](actions/get-group.md) | `GET /get_group/[:id]` | [docs](https://dev.splitwise.com/#tag/groups/paths/~1get_group~1{id}/get) |
| [Get User](actions/get-user.md) | `GET /get_user/[:id]` | [docs](https://dev.splitwise.com/#tag/users/paths/~1get_user~1{id}/get) |
| [List Expense Comments](actions/list-expense-comments.md) | `GET /get_comments` | [docs](https://dev.splitwise.com/#tag/comments/paths/~1get_comments/get) |
| [List Expenses](actions/list-expenses.md) | `GET /get_expenses` | [docs](https://dev.splitwise.com/#tag/expenses/paths/~1get_expenses/get) |
| [List Friends](actions/list-friends.md) | `GET /get_friends` | [docs](https://dev.splitwise.com/#tag/friends/paths/~1get_friends/get) |
| [List Groups](actions/list-groups.md) | `GET /get_groups` | [docs](https://dev.splitwise.com/#tag/groups/paths/~1get_groups/get) |
| [List Notifications](actions/list-notifications.md) | `GET /get_notifications` | [docs](https://dev.splitwise.com/#tag/notifications/paths/~1get_notifications/get) |
| [List Supported Categories](actions/list-supported-categories.md) | `GET /get_categories` | [docs](https://dev.splitwise.com/#tag/other/paths/~1get_categories/get) |
| [List Supported Currencies](actions/list-supported-currencies.md) | `GET /get_currencies` | [docs](https://dev.splitwise.com/#tag/other/paths/~1get_currencies/get) |
| [Restore Expense](actions/restore-expense.md) | `POST /undelete_expense/[:id]` | [docs](https://dev.splitwise.com/#tag/expenses/paths/~1undelete_expense~1{id}/post) |
| [Update Expense](actions/update-expense.md) | `POST /update_expense/[:id]` | [docs](https://dev.splitwise.com/#tag/expenses/paths/~1update_expense~1{id}/post) |
