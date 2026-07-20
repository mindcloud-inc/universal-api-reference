# Microsoft 365 Planner: Native API Reference

A consolidated summary of Microsoft 365 Planner's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/graph/api/resources/planner-overview?view=graph-rest-1.0
- **API base URL:** `https://graph.microsoft.com`

## Authentication

### Microsoft Entra OAuth2

Connect to Microsoft 365 Planner through Microsoft Graph using a Microsoft Entra OAuth 2.0 app registration.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://login.microsoftonline.com/common/oauth2/v2.0/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://login.microsoftonline.com/common/oauth2/v2.0/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `offline_access openid profile User.Read Tasks.ReadWrite GroupMember.Read.All`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://login.microsoftonline.com/common/oauth2/v2.0/token.

[Official authentication documentation](https://learn.microsoft.com/en-us/entra/identity-platform/v2-oauth2-auth-code-flow)

## API conventions

Responses from this API use JSON.

## Pagination

Use `$top` in the query string to set the page size (default 25; accepted range 1–999). Use `$skiptoken` in the query string as the pagination cursor. Follow the complete next-page URL returned by the API.

## Retry behavior

Retry responses with status codes `429,503`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Bucket](actions/create-bucket.md) | `POST /v1.0/planner/buckets` | [docs](https://learn.microsoft.com/en-us/graph/api/planner-post-buckets?view=graph-rest-1.0) |
| [Create Plan](actions/create-plan.md) | `POST /v1.0/planner/plans` | [docs](https://learn.microsoft.com/en-us/graph/api/planner-post-plans?view=graph-rest-1.0) |
| [Create Task](actions/create-task.md) | `POST /v1.0/planner/tasks` | [docs](https://learn.microsoft.com/en-us/graph/api/planner-post-tasks?view=graph-rest-1.0) |
| [Get Bucket](actions/get-bucket.md) | `GET /v1.0/planner/buckets/{{bucketId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/plannerbucket-get?view=graph-rest-1.0) |
| [Get Group](actions/get-group.md) | `GET /v1.0/groups/{{groupId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/group-get?view=graph-rest-1.0) |
| [Get My Profile](actions/get-my-profile.md) | `GET /v1.0/me` | [docs](https://learn.microsoft.com/en-us/graph/api/user-get?view=graph-rest-1.0) |
| [Get Plan](actions/get-plan.md) | `GET /v1.0/planner/plans/{{planId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/plannerplan-get?view=graph-rest-1.0) |
| [Get Plan Details](actions/get-plan-details.md) | `GET /v1.0/planner/plans/{{planId}}/details` | [docs](https://learn.microsoft.com/en-us/graph/api/plannerplandetails-get?view=graph-rest-1.0) |
| [Get Task](actions/get-task.md) | `GET /v1.0/planner/tasks/{{taskId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/plannertask-get?view=graph-rest-1.0) |
| [Get Task Details](actions/get-task-details.md) | `GET /v1.0/planner/tasks/{{taskId}}/details` | [docs](https://learn.microsoft.com/en-us/graph/api/plannertaskdetails-get?view=graph-rest-1.0) |
| [List Group Plans](actions/list-group-plans.md) | `GET /v1.0/groups/{{groupId}}/planner/plans` | [docs](https://learn.microsoft.com/en-us/graph/api/plannergroup-list-plans?view=graph-rest-1.0) |
| [List Groups](actions/list-groups.md) | `GET /v1.0/groups` | [docs](https://learn.microsoft.com/en-us/graph/api/group-list?view=graph-rest-1.0) |
| [List My Plans](actions/list-my-plans.md) | `GET /v1.0/me/planner/plans` | [docs](https://learn.microsoft.com/en-us/graph/api/planneruser-list-plans?view=graph-rest-1.0) |
| [List Plan Buckets](actions/list-plan-buckets.md) | `GET /v1.0/planner/plans/{{planId}}/buckets` | [docs](https://learn.microsoft.com/en-us/graph/api/plannerplan-list-buckets?view=graph-rest-1.0) |
| [List Plan Tasks](actions/list-plan-tasks.md) | `GET /v1.0/planner/plans/{{planId}}/tasks` | [docs](https://learn.microsoft.com/en-us/graph/api/plannerplan-list-tasks?view=graph-rest-1.0) |
