# <img src="https://images.mindcloud.co/apps/icons/unnamed-3_1774033976220.png" alt="Discourse logo" width="28" height="28"> Discourse: Universal API

Manage communities, topics, posts, and users in Discourse forums.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/discourse/latest
- **Category:** Marketing / Social Media
- **Actions:** 78
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.discourse.org
- **Vendor API docs:** https://docs.discourse.org/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Latest Topics](actions/list-latest-topics.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/list-latest-topics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (78)

### Backup

| Action | Method | Description |
| --- | --- | --- |
| [Create Backup](actions/create-backup.md) | POST | Creates a new backup in Discourse. |
| [Send Download Backup Email](actions/send-download-backup-email.md) | PUT | Sends a Discourse backup download email. |

### Badge

| Action | Method | Description |
| --- | --- | --- |
| [Create Badge](actions/create-badge.md) | POST | Creates a new badge in Discourse. |
| [Delete Badge](actions/delete-badge.md) | DELETE | Deletes an existing badge from Discourse. |
| [List User Badges](actions/list-user-badges.md) | GET | Retrieves badges for a Discourse user. |
| [Update Badge](actions/update-badge.md) | PUT | Updates an existing badge in Discourse. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | POST | Creates a new category in Discourse. |
| [Get Category](actions/get-category.md) | GET | Retrieves a forum category from Discourse. |
| [List Categories](actions/list-categories.md) | GET | Retrieves forum categories from Discourse. |
| [Update Category](actions/update-category.md) | PUT | Updates an existing category in Discourse. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Add Group Members](actions/add-group-members.md) | PUT | Adds members to a Discourse group. |
| [Create Group](actions/create-group.md) | POST | Creates a new group in Discourse. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing group from Discourse. |
| [Get Group](actions/get-group.md) | GET | Retrieves a specific group from Discourse. |
| [Get Group By Id](actions/get-group-by-id.md) | GET | Retrieves a Discourse group by ID. |
| [List Groups](actions/list-groups.md) | GET | Retrieves user groups from Discourse. |
| [Remove Group Members](actions/remove-group-members.md) | PUT | Removes members from a Discourse group. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in Discourse. |

### Invite

| Action | Method | Description |
| --- | --- | --- |
| [Create Invite](actions/create-invite.md) | POST | Creates a new invite in Discourse. |
| [Create Multiple Invites](actions/create-multiple-invites.md) | POST | Creates multiple user invites in Discourse. |
| [Invite Group To Topic](actions/invite-group-to-topic.md) | POST | Invites a group to a Discourse topic. |
| [Invite To Topic](actions/invite-to-topic.md) | POST | Invites a user to a Discourse topic. |

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [Get Notifications](actions/get-notifications.md) | GET | Retrieves notifications for the current Discourse user. |
| [Mark Notifications As Read](actions/mark-notifications-as-read.md) | PUT | Marks current Discourse notifications as read. |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Delete Post](actions/delete-post.md) | DELETE | Deletes an existing post from Discourse. |
| [Get Post](actions/get-post.md) | GET | Retrieves a single post from Discourse. |
| [Get Topic Posts](actions/get-topic-posts.md) | GET | Retrieves selected posts from a Discourse topic. |
| [Like Post](actions/like-post.md) | PUT | Adds a like to a Discourse post. |
| [List Post Replies](actions/list-post-replies.md) | GET | Retrieves replies to a Discourse post. |
| [List Posts](actions/list-posts.md) | GET | Retrieves latest posts across Discourse topics. |
| [Lock Post](actions/lock-post.md) | PUT | Locks a Discourse post from being edited. |
| [Update Post](actions/update-post.md) | PUT | Updates an existing post in Discourse. |

### Search

| Action | Method | Description |
| --- | --- | --- |
| [Search](actions/search.md) | GET | Finds Discourse content by search term. |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [Get Site Basic Info](actions/get-site-basic-info.md) | GET | Retrieves basic site information from Discourse. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a specific tag from Discourse. |
| [List Tags](actions/list-tags.md) | GET | Retrieves forum tags from Discourse. |

### Tag Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag Group](actions/create-tag-group.md) | POST | Creates a new tag group in Discourse. |
| [Update Tag Group](actions/update-tag-group.md) | PUT | Updates an existing tag group in Discourse. |

### Topic

| Action | Method | Description |
| --- | --- | --- |
| [Bookmark Topic](actions/bookmark-topic.md) | PUT | Adds a bookmark to a Discourse topic. |
| [Create Topic](actions/create-topic.md) | POST | Creates a new topic in Discourse. |
| [Delete Topic](actions/delete-topic.md) | DELETE | Deletes an existing topic from Discourse. |
| [Get Topic](actions/get-topic.md) | GET | Retrieves a single topic from Discourse. |
| [Get Topic By External ID](actions/get-topic-by-external-id.md) | GET | Retrieves a Discourse topic by external ID. |
| [List Category Topics](actions/list-category-topics.md) | GET | Retrieves topics from a Discourse category. |
| [List Latest Topics](actions/list-latest-topics.md) | GET | Retrieves the latest topics from Discourse. |
| [List Top Topics](actions/list-top-topics.md) | GET | Retrieves top Discourse topics for a selected period. |
| [Set Topic Notification Level](actions/set-topic-notification-level.md) | PUT | Updates a topic's notification level in Discourse. |
| [Update Topic](actions/update-topic.md) | PUT | Updates an existing topic in Discourse. |
| [Update Topic Status](actions/update-topic-status.md) | PUT | Updates a topic's status in Discourse. |
| [Update Topic Timestamp](actions/update-topic-timestamp.md) | PUT | Updates the timestamp of a Discourse topic. |

### Topic Timer

| Action | Method | Description |
| --- | --- | --- |
| [Create Topic Timer](actions/create-topic-timer.md) | POST | Creates a topic timer in Discourse. |

### Upload

| Action | Method | Description |
| --- | --- | --- |
| [Abort Multipart Upload](actions/abort-multipart-upload.md) | DELETE | Aborts a multipart upload in Discourse. |
| [Batch Presign Multipart Parts](actions/batch-presign-multipart-parts.md) | POST | Generates presigned URLs for multipart upload parts in Discourse. |
| [Complete External Upload](actions/complete-external-upload.md) | POST | Completes an external upload in Discourse. |
| [Complete Multipart Upload](actions/complete-multipart-upload.md) | POST | Completes a multipart upload in Discourse. |
| [Create Multipart Upload](actions/create-multipart-upload.md) | POST | Creates a multipart upload in Discourse. |
| [Create Upload](actions/create-upload.md) | POST | Creates a new upload in Discourse. |
| [Generate Presigned Put](actions/generate-presigned-put.md) | POST | Generates a presigned upload URL in Discourse. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Activate User](actions/activate-user.md) | PUT | Activates an existing user in Discourse. |
| [Anonymize User](actions/anonymize-user.md) | PUT | Anonymizes an existing user in Discourse. |
| [Change Password](actions/change-password.md) | PUT | Changes the password for a Discourse user. |
| [Create User](actions/create-user.md) | POST | Creates a new user in Discourse. |
| [Deactivate User](actions/deactivate-user.md) | PUT | Deactivates an existing user in Discourse. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes an existing user from Discourse. |
| [Get User](actions/get-user.md) | GET | Retrieves a Discourse user by username. |
| [Get User Emails](actions/get-user-emails.md) | GET | Retrieves a Discourse user's email addresses. |
| [List Group Members](actions/list-group-members.md) | GET | Retrieves members of a Discourse group. |
| [List Public Users](actions/list-public-users.md) | GET | Retrieves public forum users from Discourse. |
| [List User Actions](actions/list-user-actions.md) | GET | Retrieves recent user actions from Discourse. |
| [Log Out User](actions/log-out-user.md) | PUT | Logs an existing Discourse user out. |
| [Refresh Gravatar](actions/refresh-gravatar.md) | PUT | Refreshes the Gravatar for a Discourse user. |
| [Send Password Reset Email](actions/send-password-reset-email.md) | POST | Sends a Discourse password reset email. |
| [Silence User](actions/silence-user.md) | PUT | Silences an existing user in Discourse. |
| [Suspend User](actions/suspend-user.md) | PUT | Suspends an existing user in Discourse. |
| [Update Avatar](actions/update-avatar.md) | PUT | Updates the avatar for a Discourse user. |
| [Update Email](actions/update-email.md) | PUT | Updates a Discourse user's email address. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Discourse. |
| [Update Username](actions/update-username.md) | PUT | Updates the username for a Discourse user. |

