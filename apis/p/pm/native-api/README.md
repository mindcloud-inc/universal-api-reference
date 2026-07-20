# 5pm: Native API Reference

A consolidated summary of 5pm's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://www.5pmweb.com/help/api_docs.php
- **API base URL:** `{workspaceUrl}/api/v2`

## Authentication

### Session Login

5pm API uses login/password sign-in to obtain a session-based authenticated context for API requests.

### Credentials

- **Login:** `login` · required · 5pm login used for the authentication signIn call.
- **Workspace URL:** `workspaceUrl` · required · Tenant workspace URL used to target the correct 5pm account subdomain.

[Official authentication documentation](https://www.5pmweb.com/help/api_docs.php)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Pagination

Use `count` in the query string to set the page size. Use `offset` in the query string as the record offset.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Attach Files](actions/attach-files.md) | `POST /service/post/activity/attachFiles` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [Create Activity](actions/create-activity.md) | `POST /service/post/activity/add` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [Create Group](actions/create-group.md) | `POST /service/post/projectsgroups/add` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [Create Project](actions/create-project.md) | `POST /service/post/projects/add` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [Create Task](actions/create-task.md) | `POST /service/post/tasks/add` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [Create User](actions/create-user.md) | `POST /service/post/users/add` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [Download File](actions/download-file.md) | `POST /service/post/activity/downloadFile` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [Get Project By Id](actions/get-project-by-id.md) | `GET /service/get/projects/getById` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [Get Task By Id](actions/get-task-by-id.md) | `GET /service/get/tasks/getById` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [Get User By Email](actions/get-user-by-email.md) | `GET /service/get/users/getByEmail` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [Get User By Id](actions/get-user-by-id.md) | `GET /service/get/users/getById` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [List Activities](actions/list-activities.md) | `GET /service/get/activity/getList` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [List All Groups](actions/list-all-groups.md) | `GET /service/get/projectsgroups/getAll` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [List All Projects](actions/list-all-projects.md) | `GET /service/get/projects/getAll` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [List All Users](actions/list-all-users.md) | `GET /service/get/users/getAll` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [List Files](actions/list-files.md) | `GET /service/get/activity/getFilesList` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [List Priorities](actions/list-priorities.md) | `GET /service/get/metainfo/getPriorities` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [List Projects](actions/list-projects.md) | `GET /service/get/projects/getList` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [List Statuses](actions/list-statuses.md) | `GET /service/get/metainfo/getStatuses` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [List Tasks](actions/list-tasks.md) | `GET /service/get/tasks/getList` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [Remove Activity](actions/remove-activity.md) | `POST /service/post/activity/remove` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [Remove File](actions/remove-file.md) | `POST /service/post/activity/removeFile` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [Remove Project](actions/remove-project.md) | `POST /service/post/projects/remove` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [Remove Task](actions/remove-task.md) | `POST /service/post/tasks/remove` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [Remove User](actions/remove-user.md) | `POST /service/post/users/remove` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [Sign In](actions/sign-in.md) | `GET /service/get/authentication/signIn` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [Update Activity](actions/update-activity.md) | `POST /service/post/activity/update` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [Update Group](actions/update-group.md) | `POST /service/post/projectsgroups/update` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [Update Project](actions/update-project.md) | `POST /service/post/projects/update` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [Update Task](actions/update-task.md) | `POST /service/post/tasks/update` | [docs](https://www.5pmweb.com/help/api_docs.php) |
| [Update User](actions/update-user.md) | `POST /service/post/users/update` | [docs](https://www.5pmweb.com/help/api_docs.php) |
