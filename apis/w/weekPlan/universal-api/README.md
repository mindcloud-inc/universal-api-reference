# <img src="https://images.mindcloud.co/apps/icons/weekplan-icon-square_1776180945418.png" alt="Week Plan logo" width="28" height="28"> Week Plan: Universal API

Access Week Plan workspaces, tasks, lists, roles, plans, recurrences, and user resources through the Week Plan v2 API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/weekPlan/latest
- **Category:** Productivity / Project Management
- **Actions:** 56
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://weekplan.net
- **Vendor API docs:** https://weekplan.net/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Workspaces](actions/get-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/get-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (56)

### Action

| Action | Method | Description |
| --- | --- | --- |
| [Get Action](actions/get-action.md) | GET |  |
| [Get Actions in Date Range](actions/get-actions-in-date-range.md) | GET |  |
| [Get Day Actions](actions/get-day-actions.md) | GET |  |
| [Get High Impact Actions](actions/get-high-impact-actions.md) | GET |  |
| [Get Inbox Actions](actions/get-inbox-actions.md) | GET |  |
| [Get Meeting Actions](actions/get-meeting-actions.md) | GET |  |
| [Search Actions](actions/search-actions.md) | GET |  |

### Actions

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update Actions](actions/bulk-update-actions.md) | PUT |  |
| [Complete Action](actions/complete-action.md) | PUT |  |
| [Create Action](actions/create-action.md) | POST |  |
| [Create Promotion](actions/create-promotion.md) | POST |  |
| [Delete Action](actions/delete-action.md) | DELETE |  |
| [Delete Promotion](actions/delete-promotion.md) | DELETE |  |
| [Delete Recurrence Exception](actions/delete-recurrence-exception.md) | DELETE |  |
| [Get Actions By Repetition and Date](actions/get-actions-by-repetition-and-date.md) | GET |  |
| [Patch Action](actions/patch-action.md) | PUT |  |
| [Patch Event Action](actions/patch-event-action.md) | PUT |  |
| [Reorder Actions](actions/reorder-actions.md) | PUT |  |
| [Reorder Goal Actions](actions/reorder-goal-actions.md) | PUT |  |
| [Reorder Objective Actions](actions/reorder-objective-actions.md) | PUT |  |
| [Reorder Role Actions](actions/reorder-role-actions.md) | PUT |  |
| [Reorder Subtasks](actions/reorder-subtasks.md) | PUT |  |
| [Update Action](actions/update-action.md) | PUT |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoices](actions/get-invoices.md) | GET |  |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST |  |
| [Delete List](actions/delete-list.md) | DELETE |  |
| [Get Board Lists](actions/get-board-lists.md) | GET |  |
| [Get Lists](actions/get-lists.md) | GET |  |
| [Get Lists Raw](actions/get-lists-raw.md) | GET |  |
| [Update List](actions/update-list.md) | PUT |  |

### Objectives

| Action | Method | Description |
| --- | --- | --- |
| [Get Objective Lists](actions/get-objective-lists.md) | GET |  |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [Create Role](actions/create-role.md) | POST |  |
| [Delete Role](actions/delete-role.md) | DELETE |  |
| [Get Role Lists](actions/get-role-lists.md) | GET |  |
| [Update Default Role](actions/update-default-role.md) | PUT |  |
| [Update Role](actions/update-role.md) | PUT |  |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Get Week Plan](actions/get-week-plan.md) | GET |  |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Create Session](actions/create-session.md) | POST |  |
| [Login Session MFA](actions/login-session-mfa.md) | POST |  |
| [Logout Session](actions/logout-session.md) | DELETE |  |
| [Refresh Session Token](actions/refresh-session-token.md) | POST |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Add User Email](actions/add-user-email.md) | PUT |  |
| [Change User Email](actions/change-user-email.md) | PUT |  |
| [Deactivate User](actions/deactivate-user.md) | PUT |  |
| [Deauthorize User Email](actions/deauthorize-user-email.md) | PUT |  |
| [Delete User](actions/delete-user.md) | DELETE |  |
| [Extend User Trial](actions/extend-user-trial.md) | PUT |  |
| [Forgot Password](actions/forgot-password.md) | POST |  |
| [Get Current User](actions/get-current-user.md) | GET |  |
| [Get Pro Licenses](actions/get-pro-licenses.md) | GET |  |
| [Resend Verify Email](actions/resend-verify-email.md) | GET |  |
| [Sign Up User](actions/sign-up-user.md) | POST |  |
| [Update Password](actions/update-password.md) | PUT |  |
| [Update User](actions/update-user.md) | PUT |  |
| [Update User Product](actions/update-user-product.md) | PUT |  |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspaces](actions/get-workspaces.md) | GET |  |

