# <img src="https://images.mindcloud.co/apps/icons/liveblocks-icon_1775759287783.png" alt="Liveblocks logo" width="28" height="28"> Liveblocks: Universal API

Liveblocks REST API for rooms, comments, notifications, groups, users, and related collaboration resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/liveblocks/latest
- **Actions:** 57
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://liveblocks.io
- **Vendor API docs:** https://liveblocks.io/docs/api-reference/rest-api-endpoints

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Rooms](actions/get-rooms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/get-rooms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (57)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Get Access Token](actions/get-access-token.md) | POST | Creates an access token in Liveblocks. |
| [Get ID Token](actions/get-id-token.md) | POST | Creates an ID token in Liveblocks. |

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Get Attachment](actions/get-attachment.md) | GET | Retrieves an attachment from Liveblocks. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Add Comment Reaction](actions/add-comment-reaction.md) | POST | Creates a comment reaction in Liveblocks. |
| [Create Comment](actions/create-comment.md) | POST | Creates a new comment in Liveblocks. |
| [Delete Comment](actions/delete-comment.md) | DELETE | Deletes an existing comment from Liveblocks. |
| [Edit Comment](actions/edit-comment.md) | PUT | Updates an existing comment in Liveblocks. |
| [Edit Comment Metadata](actions/edit-comment-metadata.md) | PUT | Updates comment metadata in Liveblocks. |
| [Get Comment](actions/get-comment.md) | GET | Retrieves a comment from Liveblocks. |
| [Remove Comment Reaction](actions/remove-comment-reaction.md) | DELETE | Deletes a comment reaction from Liveblocks. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Delete Notification Settings](actions/delete-notification-settings.md) | DELETE | Deletes notification settings from Liveblocks. |
| [Delete Room Subscription Settings](actions/delete-room-subscription-settings.md) | DELETE | Deletes room subscription settings from Liveblocks. |
| [Get Notification Settings](actions/get-notification-settings.md) | GET | Retrieves notification settings from Liveblocks. |
| [Get Room Subscription Settings](actions/get-room-subscription-settings.md) | GET | Retrieves room subscription settings from Liveblocks. |
| [Get Thread Subscriptions](actions/get-thread-subscriptions.md) | GET | Retrieves thread subscriptions from Liveblocks. |
| [Get User Room Subscription Settings](actions/get-user-room-subscription-settings.md) | GET | Retrieves user room subscription settings from Liveblocks. |
| [Subscribe To Thread](actions/subscribe-to-thread.md) | PUT | Updates a Liveblocks thread subscription by subscribing a user. |
| [Unsubscribe From Thread](actions/unsubscribe-from-thread.md) | PUT | Updates a Liveblocks thread subscription by unsubscribing a user. |
| [Update Notification Settings](actions/update-notification-settings.md) | PUT | Updates notification settings in Liveblocks. |
| [Update Room Subscription Settings](actions/update-room-subscription-settings.md) | PUT | Updates room subscription settings in Liveblocks. |

### Threads

| Action | Method | Description |
| --- | --- | --- |
| [Create Thread](actions/create-thread.md) | POST | Creates a new thread in Liveblocks. |
| [Delete Thread](actions/delete-thread.md) | DELETE | Deletes an existing thread from Liveblocks. |
| [Edit Thread Metadata](actions/edit-thread-metadata.md) | PUT | Updates thread metadata in Liveblocks. |
| [Get Room Threads](actions/get-room-threads.md) | GET | Retrieves threads from a Liveblocks room. |
| [Get Thread](actions/get-thread.md) | GET | Retrieves a thread from Liveblocks. |
| [Mark Thread As Resolved](actions/mark-thread-as-resolved.md) | PUT | Marks a thread as resolved in Liveblocks. |
| [Mark Thread As Unresolved](actions/mark-thread-as-unresolved.md) | PUT | Marks a thread as unresolved in Liveblocks. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Add Group Members](actions/add-group-members.md) | PUT | Updates a Liveblocks group by adding members. |
| [Apply JSON Patch To Storage](actions/apply-json-patch-to-storage.md) | PUT | Updates Liveblocks storage with a JSON patch. |
| [Broadcast Event To Room](actions/broadcast-event-to-room.md) | POST | Broadcasts an event to a Liveblocks room. |
| [Create Group](actions/create-group.md) | POST | Creates a new group in Liveblocks. |
| [Create Room](actions/create-room.md) | POST | Creates a new room in Liveblocks. |
| [Delete All Inbox Notifications](actions/delete-all-inbox-notifications.md) | DELETE | Deletes all inbox notifications from Liveblocks. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing group from Liveblocks. |
| [Delete Inbox Notification](actions/delete-inbox-notification.md) | DELETE | Deletes an inbox notification from Liveblocks. |
| [Delete Room](actions/delete-room.md) | DELETE | Deletes an existing room from Liveblocks. |
| [Delete Storage Document](actions/delete-storage-document.md) | DELETE | Deletes a storage document from Liveblocks. |
| [Get All Inbox Notifications](actions/get-all-inbox-notifications.md) | GET | Retrieves all inbox notifications from Liveblocks. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from Liveblocks. |
| [Get Groups](actions/get-groups.md) | GET | Retrieves groups from Liveblocks. |
| [Get Inbox Notification](actions/get-inbox-notification.md) | GET | Retrieves an inbox notification from Liveblocks. |
| [Get Room](actions/get-room.md) | GET | Retrieves a room from Liveblocks. |
| [Get Rooms](actions/get-rooms.md) | GET | Retrieves rooms from Liveblocks. |
| [Get Storage Document](actions/get-storage-document.md) | GET | Retrieves a storage document from Liveblocks. |
| [Get Thread Inbox Notifications](actions/get-thread-inbox-notifications.md) | GET | Retrieves thread inbox notifications from Liveblocks. |
| [Get User Groups](actions/get-user-groups.md) | GET | Retrieves groups for a user in Liveblocks. |
| [Initialize Storage Document](actions/initialize-storage-document.md) | POST | Creates a storage document in Liveblocks. |
| [Mark Inbox Notification As Read](actions/mark-inbox-notification-as-read.md) | PUT | Marks an inbox notification as read in Liveblocks. |
| [Prewarm Room](actions/prewarm-room.md) | GET | Prewarms a room in Liveblocks. |
| [Remove Group Members](actions/remove-group-members.md) | PUT | Updates a Liveblocks group by removing members. |
| [Trigger Inbox Notification](actions/trigger-inbox-notification.md) | POST | Creates an inbox notification in Liveblocks. |
| [Update Room](actions/update-room.md) | PUT | Updates an existing room in Liveblocks. |
| [Update Room ID](actions/update-room-id.md) | PUT | Updates a room ID in Liveblocks. |
| [Update Room Organization ID](actions/update-room-organization-id.md) | PUT | Updates a room organization ID in Liveblocks. |
| [Upsert Room](actions/upsert-room.md) | PUT | Updates a room in Liveblocks, or creates it if missing. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Active Users](actions/get-active-users.md) | GET | Retrieves active users from a Liveblocks room. |
| [Set Ephemeral Presence](actions/set-ephemeral-presence.md) | PUT | Updates ephemeral presence in a Liveblocks room. |

