# Automate Team - Task Management: Native API Reference

A consolidated summary of Automate Team - Task Management's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://developers.onautomate.com/task
- **API base URL:** `https://api.automatebusiness.com`

## Authentication

### No authentication

This version uses provider read surfaces that do not require a tenant session token. Workspace-scoped arguments are supplied directly on the actions.

This API does not require request authentication.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–200). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `order` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `408,429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Task Counts](actions/get-task-counts.md) | `POST /rest/v1/rpc/get_task_counts_v52_cc` | [docs](https://developers.onautomate.com/task) |
| [List Categories](actions/list-categories.md) | `GET /rest/v1/categories` | [docs](https://developers.onautomate.com/task) |
| [List Task Users](actions/list-task-users.md) | `GET /rest/v1/user_profile` | [docs](https://developers.onautomate.com/task) |
| [List Tasks](actions/list-tasks.md) | `GET /rest/v1/t_all_tasks` | [docs](https://developers.onautomate.com/task) |
| [Lookup Workspace](actions/lookup-workspace.md) | `GET /rest/v1/api_key` | [docs](https://developers.onautomate.com/task) |
