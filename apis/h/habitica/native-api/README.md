# Habitica: Native API Reference

A consolidated summary of Habitica's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://habitica.com/apidoc/
- **API base URL:** `https://habitica.com/api/v3`

## Authentication

### Habitica API

Custom multi-header authentication for Habitica using x-api-user, x-api-key, and x-client.

### Credentials

- **User ID:** `userId` · required · Habitica user id used for the x-api-user header.
- **API Token:** `apiToken` · required · Habitica API token used for the x-api-key header.

Send these headers with each API request:

```http
x-api-key: <apiToken>
x-api-user: <userId>
```

[Official authentication documentation](https://habitica.com/apidoc/)

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Checklist Item](actions/add-checklist-item.md) | `POST /tasks/:taskId/checklist` | [docs](https://habitica.com/apidoc/#api-Task-AddChecklistItem) |
| [Add Tag To Task](actions/add-tag-to-task.md) | `POST /tasks/:taskId/tags/:tagId` | [docs](https://habitica.com/apidoc/#api-Task-AddTagToTask) |
| [Create Tag](actions/create-tag.md) | `POST /tags` | [docs](https://habitica.com/apidoc/#api-Tag-CreateTag) |
| [Create Task](actions/create-task.md) | `POST /tasks/user` | [docs](https://habitica.com/apidoc/#api-Task) |
| [Create Webhook](actions/create-webhook.md) | `POST /user/webhook` | [docs](https://habitica.com/apidoc/#api-Webhook-AddWebhook) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /tags/:tagId` | [docs](https://habitica.com/apidoc/#api-Tag-DeleteTag) |
| [Delete Task](actions/delete-task.md) | `DELETE /tasks/:taskId` | [docs](https://habitica.com/apidoc/#api-Task-DeleteTask) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /user/webhook/:id` | [docs](https://habitica.com/apidoc/#api-Webhook-UserDeleteWebhook) |
| [Get Anonymized User Data](actions/get-anonymized-user-data.md) | `GET /user/anonymized` | [docs](https://habitica.com/apidoc/#api-User-UserGetAnonymized) |
| [Get Inventory Buy List](actions/get-inventory-buy-list.md) | `GET /user/inventory/buy` | [docs](https://habitica.com/apidoc/#api-User-UserGetBuyList) |
| [Get Member](actions/get-member.md) | `GET /members/:memberId` | [docs](https://habitica.com/apidoc/#api-Member-GetMember) |
| [Get Member Achievements](actions/get-member-achievements.md) | `GET /members/:memberId/achievements` | [docs](https://habitica.com/apidoc/#api-Member-GetMemberAchievements) |
| [Get Status](actions/get-status.md) | `GET /status` | [docs](https://habitica.com/apidoc/#api-Status-GetStatus) |
| [Get Tag](actions/get-tag.md) | `GET /tags/:tagId` | [docs](https://habitica.com/apidoc/#api-Tag-GetTag) |
| [Get Task](actions/get-task.md) | `GET /tasks/:taskId` | [docs](https://habitica.com/apidoc/#api-Task-GetTask) |
| [Get User](actions/get-user.md) | `GET /user` | [docs](https://habitica.com/apidoc/#api-User-UserGet) |
| [List In-App Rewards](actions/list-in-app-rewards.md) | `GET /user/in-app-rewards` | [docs](https://habitica.com/apidoc/#api-User-UserGetInAppRewards) |
| [List Inbox Messages](actions/list-inbox-messages.md) | `GET /inbox/messages` | [docs](https://habitica.com/apidoc/#api-Inbox-GetInboxMessages) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://habitica.com/apidoc/#api-Tag-GetTags) |
| [List User Tasks](actions/list-user-tasks.md) | `GET /tasks/user` | [docs](https://habitica.com/apidoc/#api-Task-GetUserTasks) |
| [List Webhooks](actions/list-webhooks.md) | `GET /user/webhook` | [docs](https://habitica.com/apidoc/#api-Webhook-UserGetWebhook) |
| [Read Notifications](actions/read-notifications.md) | `POST /notifications/read` | [docs](https://habitica.com/apidoc/#api-Notification-ReadNotifications) |
| [Remove Checklist Item](actions/remove-checklist-item.md) | `DELETE /tasks/:taskId/checklist/:itemId` | [docs](https://habitica.com/apidoc/#api-Task-RemoveChecklistItem) |
| [Remove Tag From Task](actions/remove-tag-from-task.md) | `DELETE /tasks/:taskId/tags/:tagId` | [docs](https://habitica.com/apidoc/#api-Task-RemoveTagFromTask) |
| [Reorder Tags](actions/reorder-tags.md) | `POST /reorder-tags` | [docs](https://habitica.com/apidoc/#api-Tag-ReorderTags) |
| [Score Checklist Item](actions/score-checklist-item.md) | `POST /tasks/:taskId/checklist/:itemId/score` | [docs](https://habitica.com/apidoc/#api-Task-ScoreChecklistItem) |
| [Score Task](actions/score-task.md) | `POST /tasks/:taskId/score/:direction` | [docs](https://habitica.com/apidoc/#api-Task-ScoreTask) |
| [Send Private Message](actions/send-private-message.md) | `POST /members/send-private-message` | [docs](https://habitica.com/apidoc/#api-Member-SendPrivateMessage) |
| [Update Checklist Item](actions/update-checklist-item.md) | `PUT /tasks/:taskId/checklist/:itemId` | [docs](https://habitica.com/apidoc/#api-Task-UpdateChecklistItem) |
| [Update Tag](actions/update-tag.md) | `PUT /tags/:tagId` | [docs](https://habitica.com/apidoc/#api-Tag-UpdateTag) |
| [Update Task](actions/update-task.md) | `PUT /tasks/:taskId` | [docs](https://habitica.com/apidoc/#api-Task-UpdateTask) |
| [Update Webhook](actions/update-webhook.md) | `PUT /user/webhook/:id` | [docs](https://habitica.com/apidoc/#api-Webhook-UserUpdateWebhook) |
