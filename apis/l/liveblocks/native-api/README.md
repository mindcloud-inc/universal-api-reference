# Liveblocks: Native API Reference

A consolidated summary of Liveblocks's API configuration and 57 documented operations, with links to official documentation.

- **Official docs:** https://liveblocks.io/docs/api-reference/rest-api-endpoints
- **API base URL:** `https://api.liveblocks.io/v2`

## Authentication

### Liveblocks API Key

Authenticate Liveblocks REST API requests with a secret key sent as a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://liveblocks.io/docs/api-reference/rest-api-endpoints)

## Endpoints (57 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Comment Reaction](actions/add-comment-reaction.md) | `POST /rooms/:roomId/threads/:threadId/comments/:commentId/add-reaction` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#add-comment-reaction) |
| [Add Group Members](actions/add-group-members.md) | `POST /groups/:groupId/add-members` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#add-group-members) |
| [Apply JSON Patch To Storage](actions/apply-json-patch-to-storage.md) | `PATCH /rooms/:roomId/storage/json-patch` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#apply-json-patch-to-storage) |
| [Broadcast Event To Room](actions/broadcast-event-to-room.md) | `POST /rooms/:roomId/broadcast_event` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#broadcast-event-to-a-room) |
| [Create Comment](actions/create-comment.md) | `POST /rooms/:roomId/threads/:threadId/comments` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#create-comment) |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#create-group) |
| [Create Room](actions/create-room.md) | `POST /rooms` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#create-room) |
| [Create Thread](actions/create-thread.md) | `POST /rooms/:roomId/threads` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#create-thread) |
| [Delete All Inbox Notifications](actions/delete-all-inbox-notifications.md) | `DELETE /users/:userId/inbox-notifications` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#delete-all-inbox-notifications) |
| [Delete Comment](actions/delete-comment.md) | `DELETE /rooms/:roomId/threads/:threadId/comments/:commentId` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#delete-comment) |
| [Delete Group](actions/delete-group.md) | `DELETE /groups/:groupId` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#delete-group) |
| [Delete Inbox Notification](actions/delete-inbox-notification.md) | `DELETE /users/:userId/inbox-notifications/:inboxNotificationId` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#delete-inbox-notification) |
| [Delete Notification Settings](actions/delete-notification-settings.md) | `DELETE /users/:userId/notification-settings` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#delete-notification-settings) |
| [Delete Room](actions/delete-room.md) | `DELETE /rooms/:roomId` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#delete-room) |
| [Delete Room Subscription Settings](actions/delete-room-subscription-settings.md) | `DELETE /rooms/:roomId/users/:userId/subscription-settings` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#delete-room-subscription-settings) |
| [Delete Storage Document](actions/delete-storage-document.md) | `DELETE /rooms/:roomId/storage` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#delete-storage-document) |
| [Delete Thread](actions/delete-thread.md) | `DELETE /rooms/:roomId/threads/:threadId` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#delete-thread) |
| [Edit Comment](actions/edit-comment.md) | `POST /rooms/:roomId/threads/:threadId/comments/:commentId` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#edit-comment) |
| [Edit Comment Metadata](actions/edit-comment-metadata.md) | `POST /rooms/:roomId/threads/:threadId/comments/:commentId/metadata` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#edit-comment-metadata) |
| [Edit Thread Metadata](actions/edit-thread-metadata.md) | `POST /rooms/:roomId/threads/:threadId/metadata` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#edit-thread-metadata) |
| [Get Access Token](actions/get-access-token.md) | `POST /authorize-user` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#get-access-token-with-secret-key) |
| [Get Active Users](actions/get-active-users.md) | `GET /rooms/:roomId/active_users` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#get-active-users) |
| [Get All Inbox Notifications](actions/get-all-inbox-notifications.md) | `GET /users/:userId/inbox-notifications` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#get-all-inbox-notifications) |
| [Get Attachment](actions/get-attachment.md) | `GET /rooms/:roomId/attachments/:attachmentId` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#get-attachment) |
| [Get Comment](actions/get-comment.md) | `GET /rooms/:roomId/threads/:threadId/comments/:commentId` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#get-comment) |
| [Get Group](actions/get-group.md) | `GET /groups/:groupId` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#get-group) |
| [Get Groups](actions/get-groups.md) | `GET /groups` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#get-groups) |
| [Get ID Token](actions/get-id-token.md) | `POST /identify-user` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#get-id-token-with-secret-key) |
| [Get Inbox Notification](actions/get-inbox-notification.md) | `GET /users/:userId/inbox-notifications/:inboxNotificationId` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#get-inbox-notification) |
| [Get Notification Settings](actions/get-notification-settings.md) | `GET /users/:userId/notification-settings` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#get-notification-settings) |
| [Get Room](actions/get-room.md) | `GET /rooms/:roomId` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#get-room) |
| [Get Room Subscription Settings](actions/get-room-subscription-settings.md) | `GET /rooms/:roomId/users/:userId/subscription-settings` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#get-room-subscription-settings) |
| [Get Room Threads](actions/get-room-threads.md) | `GET /rooms/:roomId/threads` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#get-room-threads) |
| [Get Rooms](actions/get-rooms.md) | `GET /rooms` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#get-rooms) |
| [Get Storage Document](actions/get-storage-document.md) | `GET /rooms/:roomId/storage` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#get-storage-document) |
| [Get Thread](actions/get-thread.md) | `GET /rooms/:roomId/threads/:threadId` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#get-thread) |
| [Get Thread Inbox Notifications](actions/get-thread-inbox-notifications.md) | `GET /rooms/:roomId/threads/:threadId/inbox-notifications` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#get-thread-inbox-notifications) |
| [Get Thread Subscriptions](actions/get-thread-subscriptions.md) | `GET /rooms/:roomId/threads/:threadId/subscriptions` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#get-thread-subscriptions) |
| [Get User Groups](actions/get-user-groups.md) | `GET /users/:userId/groups` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#get-user-groups) |
| [Get User Room Subscription Settings](actions/get-user-room-subscription-settings.md) | `GET /users/:userId/room-subscription-settings` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#get-user-room-subscription-settings) |
| [Initialize Storage Document](actions/initialize-storage-document.md) | `POST /rooms/:roomId/storage` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#initialize-storage-document) |
| [Mark Inbox Notification As Read](actions/mark-inbox-notification-as-read.md) | `POST /inbox-notifications/:inboxNotificationId/read` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#mark-inbox-notification-as-read) |
| [Mark Thread As Resolved](actions/mark-thread-as-resolved.md) | `POST /rooms/:roomId/threads/:threadId/mark-as-resolved` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#mark-thread-as-resolved) |
| [Mark Thread As Unresolved](actions/mark-thread-as-unresolved.md) | `POST /rooms/:roomId/threads/:threadId/mark-as-unresolved` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#mark-thread-as-unresolved) |
| [Prewarm Room](actions/prewarm-room.md) | `GET /rooms/:roomId/prewarm` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#prewarm-room) |
| [Remove Comment Reaction](actions/remove-comment-reaction.md) | `POST /rooms/:roomId/threads/:threadId/comments/:commentId/remove-reaction` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#remove-comment-reaction) |
| [Remove Group Members](actions/remove-group-members.md) | `POST /groups/:groupId/remove-members` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#remove-group-members) |
| [Set Ephemeral Presence](actions/set-ephemeral-presence.md) | `POST /rooms/:roomId/presence` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#set-ephemeral-presence) |
| [Subscribe To Thread](actions/subscribe-to-thread.md) | `POST /rooms/:roomId/threads/:threadId/subscribe` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#subscribe-to-thread) |
| [Trigger Inbox Notification](actions/trigger-inbox-notification.md) | `POST /inbox-notifications/trigger` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#trigger-inbox-notification) |
| [Unsubscribe From Thread](actions/unsubscribe-from-thread.md) | `POST /rooms/:roomId/threads/:threadId/unsubscribe` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#unsubscribe-from-thread) |
| [Update Notification Settings](actions/update-notification-settings.md) | `POST /users/:userId/notification-settings` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#update-notification-settings) |
| [Update Room](actions/update-room.md) | `POST /rooms/:roomId` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#update-room) |
| [Update Room ID](actions/update-room-id.md) | `POST /rooms/:roomId/update-room-id` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#update-room-id) |
| [Update Room Organization ID](actions/update-room-organization-id.md) | `POST /rooms/:roomId/update-organization-id` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#update-room-organization-id) |
| [Update Room Subscription Settings](actions/update-room-subscription-settings.md) | `POST /rooms/:roomId/users/:userId/subscription-settings` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#update-room-subscription-settings) |
| [Upsert Room](actions/upsert-room.md) | `POST /rooms/:roomId/upsert` | [docs](https://liveblocks.io/docs/api-reference/rest-api-endpoints#upsert-update-or-create-room) |
