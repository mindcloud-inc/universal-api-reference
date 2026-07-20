# Week Plan: Native API Reference

A consolidated summary of Week Plan's API configuration and 56 documented operations, with links to official documentation.

- **Official docs:** https://weekplan.net/api/
- **API base URL:** `https://api.weekplan.net/v2`

## Authentication

### Week Plan Bearer Token

Authenticate Week Plan API requests with a bearer access token from the Week Plan session flow.

### Credentials

- **Access Token:** `accessToken` · required · A valid Week Plan bearer access token used as Authorization: Bearer <token>.

Send these headers with each API request:

```http
Authorization: Bearer <accessToken>
```

[Official authentication documentation](https://weekplan.net/api/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (56 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add User Email](actions/add-user-email.md) | `POST users/add_email` | [docs](https://weekplan.net/api/) |
| [Bulk Update Actions](actions/bulk-update-actions.md) | `POST actions/full_patch/all` | [docs](https://weekplan.net/api/) |
| [Change User Email](actions/change-user-email.md) | `POST users/change_email` | [docs](https://weekplan.net/api/) |
| [Complete Action](actions/complete-action.md) | `POST actions/complete` | [docs](https://weekplan.net/api/) |
| [Create Action](actions/create-action.md) | `POST actions` | [docs](https://weekplan.net/api/) |
| [Create List](actions/create-list.md) | `POST lists` | [docs](https://weekplan.net/api/) |
| [Create Promotion](actions/create-promotion.md) | `POST promotions` | [docs](https://weekplan.net/api/) |
| [Create Role](actions/create-role.md) | `PATCH roles/0` | [docs](https://weekplan.net/api/) |
| [Create Session](actions/create-session.md) | `POST sessions` | [docs](https://weekplan.net/api/) |
| [Deactivate User](actions/deactivate-user.md) | `POST users/deactivate` | [docs](https://weekplan.net/api/) |
| [Deauthorize User Email](actions/deauthorize-user-email.md) | `POST users/deauthorize_email` | [docs](https://weekplan.net/api/) |
| [Delete Action](actions/delete-action.md) | `DELETE actions/:actionId` | [docs](https://weekplan.net/api/) |
| [Delete List](actions/delete-list.md) | `PATCH lists/:listId` | [docs](https://weekplan.net/api/) |
| [Delete Promotion](actions/delete-promotion.md) | `DELETE promotions` | [docs](https://weekplan.net/api/) |
| [Delete Recurrence Exception](actions/delete-recurrence-exception.md) | `DELETE recurrences/:recurrenceId/exceptions` | [docs](https://weekplan.net/api/) |
| [Delete Role](actions/delete-role.md) | `PATCH roles/:roleId` | [docs](https://weekplan.net/api/) |
| [Delete User](actions/delete-user.md) | `POST users/delete` | [docs](https://weekplan.net/api/) |
| [Extend User Trial](actions/extend-user-trial.md) | `POST users/extend_trial/:userId` | [docs](https://weekplan.net/api/) |
| [Forgot Password](actions/forgot-password.md) | `POST users/forgot_password` | [docs](https://weekplan.net/api/) |
| [Get Action](actions/get-action.md) | `GET actions/:actionId` | [docs](https://weekplan.net/api/) |
| [Get Actions By Repetition and Date](actions/get-actions-by-repetition-and-date.md) | `GET actions/GetActionsByRepetitionIdAndDate` | [docs](https://weekplan.net/api/) |
| [Get Actions in Date Range](actions/get-actions-in-date-range.md) | `GET actions/timerange` | [docs](https://weekplan.net/api/) |
| [Get Board Lists](actions/get-board-lists.md) | `GET lists` | [docs](https://weekplan.net/api/) |
| [Get Current User](actions/get-current-user.md) | `GET users` | [docs](https://weekplan.net/api/) |
| [Get Day Actions](actions/get-day-actions.md) | `GET actions/day` | [docs](https://weekplan.net/api/) |
| [Get High Impact Actions](actions/get-high-impact-actions.md) | `GET actions/hits` | [docs](https://weekplan.net/api/) |
| [Get Inbox Actions](actions/get-inbox-actions.md) | `GET actions/inbox` | [docs](https://weekplan.net/api/) |
| [Get Invoices](actions/get-invoices.md) | `GET invoices` | [docs](https://weekplan.net/api/) |
| [Get Lists](actions/get-lists.md) | `GET lists/getLists` | [docs](https://weekplan.net/api/) |
| [Get Lists Raw](actions/get-lists-raw.md) | `GET lists` | [docs](https://weekplan.net/api/) |
| [Get Meeting Actions](actions/get-meeting-actions.md) | `GET actions/meetings` | [docs](https://weekplan.net/api/) |
| [Get Objective Lists](actions/get-objective-lists.md) | `GET objectives/getLists` | [docs](https://weekplan.net/api/) |
| [Get Pro Licenses](actions/get-pro-licenses.md) | `GET users/pro_licenses` | [docs](https://weekplan.net/api/) |
| [Get Role Lists](actions/get-role-lists.md) | `GET roles/getLists` | [docs](https://weekplan.net/api/) |
| [Get Week Plan](actions/get-week-plan.md) | `GET plans` | [docs](https://weekplan.net/api/) |
| [Get Workspaces](actions/get-workspaces.md) | `GET workspaces` | [docs](https://weekplan.net/api/) |
| [Login Session MFA](actions/login-session-mfa.md) | `POST sessions/login-mfa` | [docs](https://weekplan.net/api/) |
| [Logout Session](actions/logout-session.md) | `POST https://backend-api.weekplan.net/sessions/logout` | [docs](https://weekplan.net/api/) |
| [Patch Action](actions/patch-action.md) | `PATCH actions/:actionId` | [docs](https://weekplan.net/api/) |
| [Patch Event Action](actions/patch-event-action.md) | `PATCH actions/all/:actionId` | [docs](https://weekplan.net/api/) |
| [Refresh Session Token](actions/refresh-session-token.md) | `POST https://backend-api.weekplan.net/sessions/token` | [docs](https://weekplan.net/api/) |
| [Reorder Actions](actions/reorder-actions.md) | `POST actions/reorder` | [docs](https://weekplan.net/api/) |
| [Reorder Goal Actions](actions/reorder-goal-actions.md) | `POST actions/goals_reorder` | [docs](https://weekplan.net/api/) |
| [Reorder Objective Actions](actions/reorder-objective-actions.md) | `POST actions/objectives_reorder` | [docs](https://weekplan.net/api/) |
| [Reorder Role Actions](actions/reorder-role-actions.md) | `POST actions/roles_reorder` | [docs](https://weekplan.net/api/) |
| [Reorder Subtasks](actions/reorder-subtasks.md) | `POST actions/reorder_subtask` | [docs](https://weekplan.net/api/) |
| [Resend Verify Email](actions/resend-verify-email.md) | `GET users/resend_verify_email/:userId` | [docs](https://weekplan.net/api/) |
| [Search Actions](actions/search-actions.md) | `GET actions/search` | [docs](https://weekplan.net/api/) |
| [Sign Up User](actions/sign-up-user.md) | `POST users/sign-up` | [docs](https://weekplan.net/api/) |
| [Update Action](actions/update-action.md) | `POST actions/full_patch` | [docs](https://weekplan.net/api/) |
| [Update Default Role](actions/update-default-role.md) | `PATCH roles/0` | [docs](https://weekplan.net/api/) |
| [Update List](actions/update-list.md) | `PATCH lists/:listId` | [docs](https://weekplan.net/api/) |
| [Update Password](actions/update-password.md) | `POST users/password` | [docs](https://weekplan.net/api/) |
| [Update Role](actions/update-role.md) | `PATCH roles/:roleId` | [docs](https://weekplan.net/api/) |
| [Update User](actions/update-user.md) | `PATCH users/:userId` | [docs](https://weekplan.net/api/) |
| [Update User Product](actions/update-user-product.md) | `PATCH userProducts/:userProductId` | [docs](https://weekplan.net/api/) |
