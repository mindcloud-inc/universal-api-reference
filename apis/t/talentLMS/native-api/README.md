# TalentLMS: Native API Reference

A consolidated summary of TalentLMS's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/31867199/2sAY548Kou
- **API base URL:** `https://{domain}.talentlms.com/api/v2`

## Authentication

### API Key

Authenticate TalentLMS requests with your X-API-Key value.

### Credentials

- **API Key:** `apiKey` · required
- **Domain:** `domain` · required · Your TalentLMS portal subdomain host (for example sample.talentlms.com).
- **API Version:** `apiVersion` · required · TalentLMS API version header in YYYY-MM-DD format (for example 2025-12-12).

Send these headers with each API request:

```http
X-API-Key: <apiKey>
X-API-Version: <apiVersion>
```

[Official authentication documentation](https://help.talentlms.com/hc/en-us/articles/9651527213468-Can-I-integrate-my-site-with-TalentLMS-Do-you-offer-an-API)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |
| `X-API-Version` | `{{credentials.apiVersion}}` |

Responses from this API use JSON. The total page count is read from `Meta.pagination.totalPages`. The current page number is read from `Meta.pagination.page`.

## Pagination

Use `page[size]` in the query string to set the page size (default 10; accepted range 1–100). Use `page[number]` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Course to Branch](actions/add-course-to-branch.md) | `POST /branch-courses` | [docs](https://documenter.getpostman.com/view/31867199/2sAY548Kou#add-course-to-branch) |
| [Add User to Branch](actions/add-user-to-branch.md) | `POST /branch-users` | [docs](https://documenter.getpostman.com/view/31867199/2sAY548Kou#add-user-to-branch) |
| [Add User to Group](actions/add-user-to-group.md) | `POST /group-memberships/` | [docs](https://documenter.getpostman.com/view/31867199/2sAY548Kou#add-a-user-to-a-group) |
| [Create Branch](actions/create-branch.md) | `POST /branches` | [docs](https://documenter.getpostman.com/view/31867199/2sAY548Kou#create-a-branch) |
| [Create Course](actions/create-course.md) | `POST /courses` | [docs](https://documenter.getpostman.com/view/31867199/2sAY548Kou#create-course) |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://documenter.getpostman.com/view/31867199/2sAY548Kou#create-a-group) |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://documenter.getpostman.com/view/31867199/2sAY548Kou#create-a-user) |
| [Delete Branch](actions/delete-branch.md) | `DELETE /branches/:id` | [docs](https://documenter.getpostman.com/view/31867199/2sAY548Kou#delete-a-branch) |
| [Delete Course](actions/delete-course.md) | `DELETE /courses/:id` | [docs](https://documenter.getpostman.com/view/31867199/2sAY548Kou#delete-a-course) |
| [Delete Group](actions/delete-group.md) | `DELETE /groups/:id` | [docs](https://documenter.getpostman.com/view/31867199/2sAY548Kou#delete-a-group) |
| [Delete User](actions/delete-user.md) | `DELETE /users/:id` | [docs](https://documenter.getpostman.com/view/31867199/2sAY548Kou#delete-a-user) |
| [Enroll User to Course](actions/enroll-user-to-course.md) | `POST /enrollments` | [docs](https://documenter.getpostman.com/view/31867199/2sAY548Kou#enroll-user-to-course) |
| [Get Branch](actions/get-branch.md) | `GET /branches/:id` | [docs](https://documenter.getpostman.com/view/31867199/2sAY548Kou#get-a-branch) |
| [Get Course](actions/get-course.md) | `GET /courses/:id` | [docs](https://documenter.getpostman.com/view/31867199/2sAY548Kou#get-a-course) |
| [Get Group](actions/get-group.md) | `GET /groups/:id` | [docs](https://documenter.getpostman.com/view/31867199/2sAY548Kou#get-a-group) |
| [Get User](actions/get-user.md) | `GET /users/:id` | [docs](https://documenter.getpostman.com/view/31867199/2sAY548Kou#get-a-user) |
| [List Branches](actions/list-branches.md) | `GET /branches` | [docs](https://documenter.getpostman.com/view/31867199/2sAY548Kou#list-all-branches) |
| [List Courses](actions/list-courses.md) | `GET /courses` | [docs](https://documenter.getpostman.com/view/31867199/2sAY548Kou#list-all-courses) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://documenter.getpostman.com/view/31867199/2sAY548Kou#list-all-groups) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://documenter.getpostman.com/view/31867199/2sAY548Kou#list-all-users) |
| [Remove Course from Branch](actions/remove-course-from-branch.md) | `DELETE /branch-courses` | [docs](https://documenter.getpostman.com/view/31867199/2sAY548Kou#remove-course-from-branch) |
| [Remove User from Branch](actions/remove-user-from-branch.md) | `DELETE /branch-users` | [docs](https://documenter.getpostman.com/view/31867199/2sAY548Kou#remove-user-from-branch) |
| [Remove User from Course](actions/remove-user-from-course.md) | `DELETE /enrollments` | [docs](https://documenter.getpostman.com/view/31867199/2sAY548Kou#delete-a-user-from-a-course) |
| [Remove User from Group](actions/remove-user-from-group.md) | `DELETE /group-memberships/` | [docs](https://documenter.getpostman.com/view/31867199/2sAY548Kou#remove-user-from-a-group) |
| [Update User](actions/update-user.md) | `PATCH /users/:id` | [docs](https://documenter.getpostman.com/view/31867199/2sAY548Kou#update-a-user) |
