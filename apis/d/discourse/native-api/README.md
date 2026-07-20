# Discourse: Native API Reference

A consolidated summary of Discourse's API configuration and 78 documented operations, with links to official documentation.

- **Official docs:** https://docs.discourse.org/
- **OpenAPI specification:** https://docs.discourse.org/openapi.json
- **API base URL:** `https://mindcloud.discourse.group`

## Authentication

### Discourse API Credentials

Authenticate to a Discourse forum with a forum base URL, API key, and API username.

### Credentials

- **Forum Base URL:** `baseUrl` · required · The full base URL of your Discourse forum, including https://.
- **API Key:** `apiKey` · required · Your Discourse API key.
- **API Username:** `apiUsername` · required · The Discourse username associated with the API key.

Send these headers with each API request:

```http
Api-Key: <apiKey>
Api-Username: <apiUsername>
```

[Official authentication documentation](https://meta.discourse.org/t/create-and-configure-an-api-key/230124)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `api_key` | query | `string` | yes | Runtime API key query parameter for Discourse. |
| `api_username` | query | `string` | yes | Runtime API username query parameter for Discourse. |
| `baseUrl` | path | `string` | yes | Uses the connected forum base URL for all requests. |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 30; accepted range 1–100).

## Endpoints (78 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Abort Multipart Upload](actions/abort-multipart-upload.md) | `POST /uploads/abort-multipart.json` | [docs](https://docs.discourse.org/#tag/Uploads/operation/abortMultipart) |
| [Activate User](actions/activate-user.md) | `PUT /admin/users/:id/activate.json` | [docs](https://docs.discourse.org/#tag/Users/operation/activateUser) |
| [Add Group Members](actions/add-group-members.md) | `PUT /groups/:id/members.json` | [docs](https://docs.discourse.org/#tag/Groups/operation/addGroupMembers) |
| [Anonymize User](actions/anonymize-user.md) | `PUT /admin/users/:id/anonymize.json` | [docs](https://docs.discourse.org/#tag/Users/operation/anonymizeUser) |
| [Batch Presign Multipart Parts](actions/batch-presign-multipart-parts.md) | `POST /uploads/batch-presign-multipart-parts.json` | [docs](https://docs.discourse.org/#tag/Uploads/operation/batchPresignMultipartParts) |
| [Bookmark Topic](actions/bookmark-topic.md) | `PUT /t/:id/bookmark.json` | [docs](https://docs.discourse.org/#tag/Topics/operation/bookmarkTopic) |
| [Change Password](actions/change-password.md) | `PUT /users/password-reset/:token.json` | [docs](https://docs.discourse.org/#tag/Users/operation/changePassword) |
| [Complete External Upload](actions/complete-external-upload.md) | `POST /uploads/complete-external-upload.json` | [docs](https://docs.discourse.org/#tag/Uploads/operation/completeExternalUpload) |
| [Complete Multipart Upload](actions/complete-multipart-upload.md) | `POST /uploads/complete-multipart.json` | [docs](https://docs.discourse.org/#tag/Uploads/operation/completeMultipart) |
| [Create Backup](actions/create-backup.md) | `POST /admin/backups.json` | [docs](https://docs.discourse.org/#tag/Backups/operation/createBackup) |
| [Create Badge](actions/create-badge.md) | `POST /admin/badges.json` | [docs](https://docs.discourse.org/#tag/Badges/operation/createBadge) |
| [Create Category](actions/create-category.md) | `POST /categories.json` | [docs](https://docs.discourse.org/#tag/Categories/operation/createCategory) |
| [Create Group](actions/create-group.md) | `POST /admin/groups.json` | [docs](https://docs.discourse.org/#tag/Groups/operation/createGroup) |
| [Create Invite](actions/create-invite.md) | `POST /invites.json` | [docs](https://docs.discourse.org/#tag/Invites/operation/createInvite) |
| [Create Multipart Upload](actions/create-multipart-upload.md) | `POST /uploads/create-multipart.json` | [docs](https://docs.discourse.org/#tag/Uploads/operation/createMultipartUpload) |
| [Create Multiple Invites](actions/create-multiple-invites.md) | `POST /invites/create-multiple.json` | [docs](https://docs.discourse.org/#tag/Invites/operation/createMultipleInvites) |
| [Create Tag Group](actions/create-tag-group.md) | `POST /tag_groups.json` | [docs](https://docs.discourse.org/#tag/Tags/operation/createTagGroup) |
| [Create Topic](actions/create-topic.md) | `POST /posts.json` | [docs](https://docs.discourse.org/#tag/Posts/operation/createTopicPostPM) |
| [Create Topic Timer](actions/create-topic-timer.md) | `POST /t/:id/timer.json` | [docs](https://docs.discourse.org/#tag/Topics/operation/createTopicTimer) |
| [Create Upload](actions/create-upload.md) | `POST /uploads.json` | [docs](https://docs.discourse.org/#tag/Uploads/operation/createUpload) |
| [Create User](actions/create-user.md) | `POST /users.json` | [docs](https://docs.discourse.org/#tag/Users/operation/createUser) |
| [Deactivate User](actions/deactivate-user.md) | `PUT /admin/users/:id/deactivate.json` | [docs](https://docs.discourse.org/#tag/Users/operation/deactivateUser) |
| [Delete Badge](actions/delete-badge.md) | `DELETE /admin/badges/:id.json` | [docs](https://docs.discourse.org/#tag/Badges/operation/deleteBadge) |
| [Delete Group](actions/delete-group.md) | `DELETE /admin/groups/:id.json` | [docs](https://docs.discourse.org/#tag/Groups/operation/deleteGroup) |
| [Delete Post](actions/delete-post.md) | `DELETE /posts/:id.json` | [docs](https://docs.discourse.org/#tag/Posts/operation/deletePost) |
| [Delete Topic](actions/delete-topic.md) | `DELETE /t/:id.json` | [docs](https://docs.discourse.org/#tag/Topics/operation/removeTopic) |
| [Delete User](actions/delete-user.md) | `DELETE /admin/users/:id.json` | [docs](https://docs.discourse.org/#tag/Users/operation/deleteUser) |
| [Generate Presigned Put](actions/generate-presigned-put.md) | `POST /uploads/generate-presigned-put.json` | [docs](https://docs.discourse.org/#tag/Uploads/operation/generatePresignedPut) |
| [Get Category](actions/get-category.md) | `GET /c/:id/show.json` | [docs](https://docs.discourse.org/#tag/Categories/operation/getCategory) |
| [Get Group](actions/get-group.md) | `GET /groups/:name.json` | [docs](https://docs.discourse.org/#tag/Groups/operation/getGroup) |
| [Get Group By Id](actions/get-group-by-id.md) | `GET /groups/by-id/:id.json` | [docs](https://docs.discourse.org/#tag/Groups/operation/getGroupById) |
| [Get Notifications](actions/get-notifications.md) | `GET /notifications.json` | [docs](https://docs.discourse.org/#tag/Notifications/operation/getNotifications) |
| [Get Post](actions/get-post.md) | `GET /posts/:id.json` | [docs](https://docs.discourse.org/#tag/Posts/operation/getPost) |
| [Get Site Basic Info](actions/get-site-basic-info.md) | `GET /site/basic-info.json` | [docs](https://docs.discourse.org/#tag/Site/operation/getSiteBasicInfo) |
| [Get Tag](actions/get-tag.md) | `GET /tag/:name.json` | [docs](https://docs.discourse.org/#tag/Tags/operation/getTag) |
| [Get Topic](actions/get-topic.md) | `GET /t/:id.json` | [docs](https://docs.discourse.org/#tag/Topics/operation/getTopic) |
| [Get Topic By External ID](actions/get-topic-by-external-id.md) | `GET /t/external_id/:external_id.json` | [docs](https://docs.discourse.org/#tag/Topics/operation/getTopicByExternalId) |
| [Get Topic Posts](actions/get-topic-posts.md) | `GET /t/:id/posts.json` | [docs](https://docs.discourse.org/#tag/Topics/operation/getSpecificPostsFromTopic) |
| [Get User](actions/get-user.md) | `GET /u/:username.json` | [docs](https://docs.discourse.org/#tag/Users/operation/getUser) |
| [Get User Emails](actions/get-user-emails.md) | `GET /u/:username/emails.json` | [docs](https://docs.discourse.org/#tag/Users/operation/getUserEmails) |
| [Invite Group To Topic](actions/invite-group-to-topic.md) | `POST /t/:id/invite-group.json` | [docs](https://docs.discourse.org/#tag/Topics/operation/inviteGroupToTopic) |
| [Invite To Topic](actions/invite-to-topic.md) | `POST /t/:id/invite.json` | [docs](https://docs.discourse.org/#tag/Topics/operation/inviteToTopic) |
| [Like Post](actions/like-post.md) | `POST /post_actions.json` | [docs](https://docs.discourse.org/#tag/Posts/operation/performPostAction) |
| [List Categories](actions/list-categories.md) | `GET /categories.json` | [docs](https://docs.discourse.org/#tag/Categories/operation/listCategories) |
| [List Category Topics](actions/list-category-topics.md) | `GET /c/:slug/:id.json` | [docs](https://docs.discourse.org/#tag/Categories/operation/listCategoryTopics) |
| [List Group Members](actions/list-group-members.md) | `GET /groups/:name/members.json` | [docs](https://docs.discourse.org/#tag/Groups/operation/listGroupMembers) |
| [List Groups](actions/list-groups.md) | `GET /groups.json` | [docs](https://docs.discourse.org/#tag/Groups/operation/listGroups) |
| [List Latest Topics](actions/list-latest-topics.md) | `GET /latest.json` | [docs](https://docs.discourse.org/#tag/Topics/operation/listLatestTopics) |
| [List Post Replies](actions/list-post-replies.md) | `GET /posts/:id/replies.json` | [docs](https://docs.discourse.org/#tag/Posts/operation/postReplies) |
| [List Posts](actions/list-posts.md) | `GET /posts.json` | [docs](https://docs.discourse.org/#tag/Posts/operation/listPosts) |
| [List Public Users](actions/list-public-users.md) | `GET /directory_items.json` | [docs](https://docs.discourse.org/#tag/Users/operation/listUsersPublic) |
| [List Tags](actions/list-tags.md) | `GET /tags.json` | [docs](https://docs.discourse.org/#tag/Tags/operation/listTags) |
| [List Top Topics](actions/list-top-topics.md) | `GET /top.json` | [docs](https://docs.discourse.org/#tag/Topics/operation/listTopTopics) |
| [List User Actions](actions/list-user-actions.md) | `GET /user_actions.json` | [docs](https://docs.discourse.org/#tag/Users/operation/listUserActions) |
| [List User Badges](actions/list-user-badges.md) | `GET /user-badges/:username.json` | [docs](https://docs.discourse.org/#tag/Badges/operation/listUserBadges) |
| [Lock Post](actions/lock-post.md) | `PUT /posts/:id/locked.json` | [docs](https://docs.discourse.org/#tag/Posts/operation/lockPost) |
| [Log Out User](actions/log-out-user.md) | `POST /admin/users/:id/log_out.json` | [docs](https://docs.discourse.org/#tag/Users/operation/logOutUser) |
| [Mark Notifications As Read](actions/mark-notifications-as-read.md) | `PUT /notifications/mark-read.json` | [docs](https://docs.discourse.org/#tag/Notifications/operation/markNotificationsAsRead) |
| [Refresh Gravatar](actions/refresh-gravatar.md) | `POST /user_avatar/:username/refresh_gravatar.json` | [docs](https://docs.discourse.org/#tag/Users/operation/refreshGravatar) |
| [Remove Group Members](actions/remove-group-members.md) | `DELETE /groups/:id/members.json` | [docs](https://docs.discourse.org/#tag/Groups/operation/removeGroupMembers) |
| [Search](actions/search.md) | `GET /search.json` | [docs](https://docs.discourse.org/#tag/Search/operation/search) |
| [Send Download Backup Email](actions/send-download-backup-email.md) | `PUT /admin/backups/:filename` | [docs](https://docs.discourse.org/#tag/Backups/operation/sendDownloadBackupEmail) |
| [Send Password Reset Email](actions/send-password-reset-email.md) | `POST /session/forgot_password.json` | [docs](https://docs.discourse.org/#tag/Users/operation/sendPasswordResetEmail) |
| [Set Topic Notification Level](actions/set-topic-notification-level.md) | `POST /t/:id/notifications.json` | [docs](https://docs.discourse.org/#tag/Topics/operation/setNotificationLevel) |
| [Silence User](actions/silence-user.md) | `PUT /admin/users/:id/silence.json` | [docs](https://docs.discourse.org/#tag/Users/operation/silenceUser) |
| [Suspend User](actions/suspend-user.md) | `PUT /admin/users/:id/suspend.json` | [docs](https://docs.discourse.org/#tag/Users/operation/suspendUser) |
| [Update Avatar](actions/update-avatar.md) | `PUT /u/:username/preferences/avatar/pick.json` | [docs](https://docs.discourse.org/#tag/Users/operation/updateAvatar) |
| [Update Badge](actions/update-badge.md) | `PUT /admin/badges/:id.json` | [docs](https://docs.discourse.org/#tag/Badges/operation/updateBadge) |
| [Update Category](actions/update-category.md) | `PUT /categories/:id.json` | [docs](https://docs.discourse.org/#tag/Categories/operation/updateCategory) |
| [Update Email](actions/update-email.md) | `PUT /u/:username/preferences/email.json` | [docs](https://docs.discourse.org/#tag/Users/operation/updateEmail) |
| [Update Group](actions/update-group.md) | `PUT /groups/:id.json` | [docs](https://docs.discourse.org/#tag/Groups/operation/updateGroup) |
| [Update Post](actions/update-post.md) | `PUT /posts/:id.json` | [docs](https://docs.discourse.org/#tag/Posts/operation/updatePost) |
| [Update Tag Group](actions/update-tag-group.md) | `PUT /tag_groups/:id.json` | [docs](https://docs.discourse.org/#tag/Tags/operation/updateTagGroup) |
| [Update Topic](actions/update-topic.md) | `PUT /t/-/:id.json` | [docs](https://docs.discourse.org/#tag/Topics/operation/updateTopic) |
| [Update Topic Status](actions/update-topic-status.md) | `PUT /t/:id/status.json` | [docs](https://docs.discourse.org/#tag/Topics/operation/updateTopicStatus) |
| [Update Topic Timestamp](actions/update-topic-timestamp.md) | `PUT /t/:id/change-timestamp.json` | [docs](https://docs.discourse.org/#tag/Topics/operation/updateTopicTimestamp) |
| [Update User](actions/update-user.md) | `PUT /u/:username.json` | [docs](https://docs.discourse.org/#tag/Users/operation/updateUser) |
| [Update Username](actions/update-username.md) | `PUT /u/:username/preferences/username.json` | [docs](https://docs.discourse.org/#tag/Users/operation/updateUsername) |
