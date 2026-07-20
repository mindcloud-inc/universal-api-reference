# Jooto: Native API Reference

A consolidated summary of Jooto's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://www.jooto.com/api/reference/
- **API base URL:** `https://app.jooto.com`

## Authentication

### API Key

Use a Jooto API key passed in the X-Jooto-Api-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Jooto-Api-Key: <apiKey>
```

[Official authentication documentation](https://www.jooto.com/api/reference/authentication/)

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Board](actions/get-board.md) | `GET /api/v1/boards/:id` | [docs](https://www.jooto.com/api/reference/request/) |
| [Get Category](actions/get-category.md) | `GET /api/v1/categories/:id` | [docs](https://www.jooto.com/api/reference/request/) |
| [Get Notification](actions/get-notification.md) | `GET /api/v1/notifications/:id` | [docs](https://www.jooto.com/api/reference/request/) |
| [Get Notification Settings](actions/get-notification-settings.md) | `GET /api/v1/notifications/get_settings` | [docs](https://www.jooto.com/api/reference/request/) |
| [Get Organization](actions/get-organization.md) | `GET /api/v1/organizations/:id` | [docs](https://www.jooto.com/api/reference/request/) |
| [Get Public Board](actions/get-public-board.md) | `GET /api/public/v1/boards/:id` | [docs](https://www.jooto.com/api/reference/request/) |
| [Get Public Board Notification Config](actions/get-public-board-notification-config.md) | `GET /api/public/v1/boards/:id/notification_config` | [docs](https://www.jooto.com/api/reference/request/) |
| [Get Public User](actions/get-public-user.md) | `GET /api/public/v1/users/:id` | [docs](https://www.jooto.com/api/reference/request/) |
| [Get Public User Role](actions/get-public-user-role.md) | `GET /api/public/v1/users/:id/role` | [docs](https://www.jooto.com/api/reference/request/) |
| [Get Rate Limit](actions/get-rate-limit.md) | `GET /api/public/v1/rate_limit` | [docs](https://www.jooto.com/api/reference/restriction/) |
| [Get Task](actions/get-task.md) | `GET /api/v1/tasks/:id` | [docs](https://www.jooto.com/api/reference/request/) |
| [Get Unread Notification Count](actions/get-unread-notification-count.md) | `GET /api/v1/notifications/get_number_of_unread_notifications` | [docs](https://www.jooto.com/api/reference/request/) |
| [Get Unread System Notification Count](actions/get-unread-system-notification-count.md) | `GET /api/v1/system_notifications/get_number_of_unread_system_notifications` | [docs](https://www.jooto.com/api/reference/request/) |
| [List Board Activities](actions/list-board-activities.md) | `GET /api/v1/boards/:board_id/activities` | [docs](https://www.jooto.com/api/reference/request/) |
| [List Board Lists](actions/list-board-lists.md) | `GET /api/v1/boards/:board_id/lists` | [docs](https://www.jooto.com/api/reference/request/) |
| [List Boards](actions/list-boards.md) | `GET /api/v1/boards` | [docs](https://www.jooto.com/api/reference/request/) |
| [List Categories](actions/list-categories.md) | `GET /api/v1/categories` | [docs](https://www.jooto.com/api/reference/request/) |
| [List Favorite Boards](actions/list-favorite-boards.md) | `GET /api/v1/favorite_boards` | [docs](https://www.jooto.com/api/reference/request/) |
| [List My Tasks](actions/list-my-tasks.md) | `GET /api/v1/my_tasks` | [docs](https://www.jooto.com/api/reference/request/) |
| [List Notification Types](actions/list-notification-types.md) | `GET /api/v1/notifications/get_notification_types` | [docs](https://www.jooto.com/api/reference/request/) |
| [List Notifications](actions/list-notifications.md) | `GET /api/v1/notifications` | [docs](https://www.jooto.com/api/reference/request/) |
| [List Organizations](actions/list-organizations.md) | `GET /api/v1/organizations` | [docs](https://www.jooto.com/api/reference/request/) |
| [List Public Board Activities](actions/list-public-board-activities.md) | `GET /api/public/v1/boards/:id/activities` | [docs](https://www.jooto.com/api/reference/request/) |
| [List Public Board Attachments](actions/list-public-board-attachments.md) | `GET /api/public/v1/boards/:id/attachments` | [docs](https://www.jooto.com/api/reference/request/) |
| [List Public Board Lists](actions/list-public-board-lists.md) | `GET /api/public/v1/boards/:board_id/lists` | [docs](https://www.jooto.com/api/reference/request/) |
| [List Public Board Tasks](actions/list-public-board-tasks.md) | `GET /api/public/v1/boards/:board_id/tasks` | [docs](https://www.jooto.com/api/reference/request/) |
| [List Public Board Users](actions/list-public-board-users.md) | `GET /api/public/v1/boards/:board_id/users` | [docs](https://www.jooto.com/api/reference/request/) |
| [List Public Boards](actions/list-public-boards.md) | `GET /api/public/v1/boards` | [docs](https://www.jooto.com/api/reference/request/) |
| [List Public Favorite Boards](actions/list-public-favorite-boards.md) | `GET /api/public/v1/boards/favorites` | [docs](https://www.jooto.com/api/reference/request/) |
| [List Public Notifications](actions/list-public-notifications.md) | `GET /api/public/v1/notifications` | [docs](https://www.jooto.com/api/reference/request/) |
| [List Public Task Checklists](actions/list-public-task-checklists.md) | `GET /api/public/v1/tasks/:task_id/checklists` | [docs](https://www.jooto.com/api/reference/request/) |
| [List Public Task Comments](actions/list-public-task-comments.md) | `GET /api/public/v1/tasks/:task_id/comments` | [docs](https://www.jooto.com/api/reference/request/) |
| [List Public Users](actions/list-public-users.md) | `GET /api/public/v1/users` | [docs](https://www.jooto.com/api/reference/request/) |
| [List System Notifications](actions/list-system-notifications.md) | `GET /api/v1/system_notifications` | [docs](https://www.jooto.com/api/reference/request/) |
| [List Task Activities](actions/list-task-activities.md) | `GET /api/v1/tasks/:task_id/activities` | [docs](https://www.jooto.com/api/reference/request/) |
| [List Task Checklists](actions/list-task-checklists.md) | `GET /api/v1/tasks/:task_id/checklists` | [docs](https://www.jooto.com/api/reference/request/) |
| [List Task Comments](actions/list-task-comments.md) | `GET /api/v1/tasks/:task_id/comments` | [docs](https://www.jooto.com/api/reference/request/) |
| [List Tasks](actions/list-tasks.md) | `GET /api/v1/tasks` | [docs](https://www.jooto.com/api/reference/request/) |
| [Search Public Board](actions/search-public-board.md) | `GET /api/public/v1/boards/:id/search` | [docs](https://www.jooto.com/api/reference/request/) |
| [Search Tasks](actions/search-tasks.md) | `GET /api/v1/tasks/search` | [docs](https://www.jooto.com/api/reference/request/) |
