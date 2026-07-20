# Weekdone: Native API Reference

A consolidated summary of Weekdone's API configuration and 37 documented operations, with links to official documentation.

- **Official docs:** https://weekdone.com/developer
- **API base URL:** `https://api.weekdone.com/1/`

## Authentication

### OAuth 2.0

Connect Weekdone with OAuth 2.0 Authorization Code flow.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://weekdone.com/oauth_authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://weekdone.com/oauth_token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://weekdone.com/oauth_token.

[Official authentication documentation](https://weekdone.com/developer)

## API conventions

Response data is read from `data`.

## Endpoints (37 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Item Comment](actions/add-item-comment.md) | `POST item/:itemId/comments` | [docs](https://weekdone.com/developer#h-items) |
| [Add Item Like](actions/add-item-like.md) | `POST item/:itemId/likes` | [docs](https://weekdone.com/developer#h-items) |
| [Add Objective Comment](actions/add-objective-comment.md) | `POST objective/:objectiveId/comments` | [docs](https://weekdone.com/developer#h-objectives) |
| [Add Objective Result](actions/add-objective-result.md) | `POST objective/:objectiveId/result` | [docs](https://weekdone.com/developer#h-key-results) |
| [Assign Item](actions/assign-item.md) | `PATCH item/:itemId/assign` | [docs](https://weekdone.com/developer#h-items) |
| [Create Item](actions/create-item.md) | `POST item` | [docs](https://weekdone.com/developer#h-items) |
| [Create KPI](actions/create-kpi.md) | `POST kpi` | [docs](https://weekdone.com/developer#h-kpis) |
| [Create Objective](actions/create-objective.md) | `POST objective` | [docs](https://weekdone.com/developer#h-objectives) |
| [Delete Item](actions/delete-item.md) | `DELETE item/:itemId` | [docs](https://weekdone.com/developer#h-items) |
| [Delete Item Comment](actions/delete-item-comment.md) | `DELETE item/:itemId/comments/:commentId` | [docs](https://weekdone.com/developer#h-items) |
| [Delete Item Like](actions/delete-item-like.md) | `DELETE item/:itemId/likes` | [docs](https://weekdone.com/developer#h-items) |
| [Delete KPI](actions/delete-kpi.md) | `DELETE kpi/:kpiId` | [docs](https://weekdone.com/developer#h-kpis) |
| [Delete Objective](actions/delete-objective.md) | `DELETE objective/:objectiveId` | [docs](https://weekdone.com/developer#h-objectives) |
| [Delete Objective Comment](actions/delete-objective-comment.md) | `DELETE objective/:objectiveId/comments/:commentId` | [docs](https://weekdone.com/developer#h-objectives) |
| [Delete Objective Result](actions/delete-objective-result.md) | `DELETE objective/:objectiveId/result/:resultId` | [docs](https://weekdone.com/developer#h-key-results) |
| [Get Company Info](actions/get-company-info.md) | `GET company` | [docs](https://weekdone.com/developer#h-company-details) |
| [Get Report](actions/get-report.md) | `GET report` | [docs](https://weekdone.com/developer#h-report) |
| [Get Tag](actions/get-tag.md) | `GET tag/:tagId` | [docs](https://weekdone.com/developer#h-tags) |
| [List Item Comments](actions/list-item-comments.md) | `GET item/:itemId/comments` | [docs](https://weekdone.com/developer#h-items) |
| [List Item Likes](actions/list-item-likes.md) | `GET item/:itemId/likes` | [docs](https://weekdone.com/developer#h-items) |
| [List KPIs](actions/list-kpis.md) | `GET kpi` | [docs](https://weekdone.com/developer#h-kpis) |
| [List Objective Comments](actions/list-objective-comments.md) | `GET objective/:objectiveId/comments` | [docs](https://weekdone.com/developer#h-objectives) |
| [List Objectives](actions/list-objectives.md) | `GET objective` | [docs](https://weekdone.com/developer#h-objectives) |
| [List Tags](actions/list-tags.md) | `GET tag` | [docs](https://weekdone.com/developer#h-tags) |
| [List Teams](actions/list-teams.md) | `GET teams` | [docs](https://weekdone.com/developer#h-teams) |
| [List Types](actions/list-types.md) | `GET types` | [docs](https://weekdone.com/developer#h-types) |
| [List Users](actions/list-users.md) | `GET users` | [docs](https://weekdone.com/developer#h-users) |
| [Search Items](actions/search-items.md) | `GET items` | [docs](https://weekdone.com/developer#h-items) |
| [Sort Items](actions/sort-items.md) | `POST item/:itemId/sort` | [docs](https://weekdone.com/developer#h-items) |
| [Update Item](actions/update-item.md) | `PATCH item/:itemId` | [docs](https://weekdone.com/developer#h-items) |
| [Update KPI](actions/update-kpi.md) | `PATCH kpi/:kpiId` | [docs](https://weekdone.com/developer#h-kpis) |
| [Update KPI Value](actions/update-kpi-value.md) | `POST kpi/:kpiId/progress` | [docs](https://weekdone.com/developer#h-kpis) |
| [Update Objective](actions/update-objective.md) | `PATCH objective/:objectiveId` | [docs](https://weekdone.com/developer#h-objectives) |
| [Update Objective Comment](actions/update-objective-comment.md) | `PATCH objective/:objectiveId/comments/:commentId` | [docs](https://weekdone.com/developer#h-objectives) |
| [Update Objective Result](actions/update-objective-result.md) | `PATCH objective/:objectiveId/result/:resultId` | [docs](https://weekdone.com/developer#h-key-results) |
| [Update Tag Priority](actions/update-tag-priority.md) | `PATCH tag/:tagId/priority` | [docs](https://weekdone.com/developer#h-tags) |
| [Update Tag Status](actions/update-tag-status.md) | `PATCH tag/:tagId/status` | [docs](https://weekdone.com/developer#h-tags) |
