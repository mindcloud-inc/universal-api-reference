# <img src="https://images.mindcloud.co/apps/icons/nextcloud-ocs-icon_1776773268540.png" alt="Next Cloud OCS logo" width="28" height="28"> Next Cloud OCS: Universal API

Access Nextcloud Open Collaboration Services (OCS) endpoints for capabilities, sharing, sharee lookup, user preferences, user status, recommendations, and other tenant APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nextCloudOCS/latest
- **Category:** Content & Files / Storage
- **Actions:** 383
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://nextcloud.com
- **Vendor API docs:** https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-api-overview.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Capabilities](actions/get-capabilities.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/get-capabilities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (383)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Activity](actions/list-activity.md) | GET | Retrieves activity from Next Cloud OCS. |
| [List Activity By Filter](actions/list-activity-by-filter.md) | GET | Retrieves activity by filter from Next Cloud OCS. |

### Activity Filter

| Action | Method | Description |
| --- | --- | --- |
| [List Activity Filters](actions/list-activity-filters.md) | GET | Retrieves activity filters from Next Cloud OCS. |

### Admin Notification

| Action | Method | Description |
| --- | --- | --- |
| [Create Admin Notification](actions/create-admin-notification.md) | POST | Creates an new admin notification in Next Cloud OCS. |

### App

| Action | Method | Description |
| --- | --- | --- |
| [Disable App](actions/disable-app.md) | PUT | Disables an app in Next Cloud OCS. |
| [Enable App](actions/enable-app.md) | PUT | Enables an app in Next Cloud OCS. |
| [List Apps](actions/list-apps.md) | GET | Retrieves apps from Next Cloud OCS. |

### App Info

| Action | Method | Description |
| --- | --- | --- |
| [Get App Info](actions/get-app-info.md) | GET | Retrieves app details from Next Cloud OCS. |

### Autocomplete Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Core Autocomplete](actions/search-core-autocomplete.md) | GET | Finds core autocomplete in Next Cloud OCS. |

### Backup Status

| Action | Method | Description |
| --- | --- | --- |
| [Restore Backup Status](actions/restore-backup-status.md) | DELETE | Restores a backup status in Next Cloud OCS. |

### Capabilities

| Action | Method | Description |
| --- | --- | --- |
| [Get Capabilities](actions/get-capabilities.md) | GET | Retrieves capabilities from Next Cloud OCS. |

### Contact Import

| Action | Method | Description |
| --- | --- | --- |
| [Import Contacts File](actions/import-contacts-file.md) | POST | Imports a contacts file into Next Cloud OCS. |

### Current User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Next Cloud OCS. |

### Direct Download Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Direct Download Link](actions/create-direct-download-link.md) | POST | Creates a new direct download link in Next Cloud OCS. |

### Direct Editing Capabilities

| Action | Method | Description |
| --- | --- | --- |
| [Get Direct Editing Capabilities](actions/get-direct-editing-capabilities.md) | GET | Retrieves direct editing capabilities from Next Cloud OCS. |

### Direct Editing File

| Action | Method | Description |
| --- | --- | --- |
| [Create Direct Editing File](actions/create-direct-editing-file.md) | POST | Creates a new direct editing file in Next Cloud OCS. |
| [Open Direct Editing File](actions/open-direct-editing-file.md) | POST | Opens a direct editing file in Next Cloud OCS. |

### Editable User Field

| Action | Method | Description |
| --- | --- | --- |
| [List Editable User Fields](actions/list-editable-user-fields.md) | GET | Retrieves editable user fields from Next Cloud OCS. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in Next Cloud OCS. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes a group from Next Cloud OCS. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from Next Cloud OCS. |

### Group Member

| Action | Method | Description |
| --- | --- | --- |
| [Get Group Members](actions/get-group-members.md) | GET | Retrieves group members from Next Cloud OCS. |

### Inherited Share

| Action | Method | Description |
| --- | --- | --- |
| [List Inherited Shares](actions/list-inherited-shares.md) | GET | Retrieves inherited shares from Next Cloud OCS. |

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [Delete All Notifications](actions/delete-all-notifications.md) | DELETE | Deletes all notifications from Next Cloud OCS. |
| [Delete Notification](actions/delete-notification.md) | DELETE | Deletes a notification from Next Cloud OCS. |
| [Get Notification](actions/get-notification.md) | GET | Retrieves notification from Next Cloud OCS. |
| [List Notifications](actions/list-notifications.md) | GET | Retrieves notifications from Next Cloud OCS. |

### Notification Existence

| Action | Method | Description |
| --- | --- | --- |
| [Check Notifications Exist](actions/check-notifications-exist.md) | GET | Checks whether notifications exist in Next Cloud OCS. |

### Out Of Office

| Action | Method | Description |
| --- | --- | --- |
| [Clear Out Of Office](actions/clear-out-of-office.md) | DELETE | Clears out-of-office settings in Next Cloud OCS. |
| [Get Current Out Of Office](actions/get-current-out-of-office.md) | GET | Retrieves current out-of-office settings from Next Cloud OCS. |
| [Get Upcoming Out Of Office](actions/get-upcoming-out-of-office.md) | GET | Retrieves upcoming out-of-office settings from Next Cloud OCS. |
| [Update Out Of Office](actions/update-out-of-office.md) | PUT | Updates out-of-office settings in Next Cloud OCS. |

### Path Share

| Action | Method | Description |
| --- | --- | --- |
| [Get Shares For Path](actions/get-shares-for-path.md) | GET | Retrieves shares for a path from Next Cloud OCS. |

### Pending Remote Share

| Action | Method | Description |
| --- | --- | --- |
| [Accept Pending Remote Share](actions/accept-pending-remote-share.md) | PUT | Accepts a pending remote share in Next Cloud OCS. |
| [Decline Pending Remote Share](actions/decline-pending-remote-share.md) | DELETE | Declines a pending remote share in Next Cloud OCS. |
| [List Pending Remote Shares](actions/list-pending-remote-shares.md) | GET | Retrieves pending remote shares from Next Cloud OCS. |

### Pending Share

| Action | Method | Description |
| --- | --- | --- |
| [List Pending Shares](actions/list-pending-shares.md) | GET | Retrieves pending shares from Next Cloud OCS. |

### Predefined Status

| Action | Method | Description |
| --- | --- | --- |
| [List Predefined Statuses](actions/list-predefined-statuses.md) | GET | Retrieves predefined statuses from Next Cloud OCS. |

### Push Device

| Action | Method | Description |
| --- | --- | --- |
| [Register Push Device](actions/register-push-device.md) | POST | Registers a push device in Next Cloud OCS. |
| [Unregister Push Device](actions/unregister-push-device.md) | DELETE | Unregisters a push device from Next Cloud OCS. |

### Recommendation

| Action | Method | Description |
| --- | --- | --- |
| [Get All Recommendations](actions/get-all-recommendations.md) | GET | Retrieves all recommendations from Next Cloud OCS. |
| [Get Recommendations](actions/get-recommendations.md) | GET | Retrieves recommendations from Next Cloud OCS. |

### Recommended Sharee

| Action | Method | Description |
| --- | --- | --- |
| [List Sharee Recommendations](actions/list-sharee-recommendations.md) | GET | Retrieves sharee recommendations from Next Cloud OCS. |

### Remote Share

| Action | Method | Description |
| --- | --- | --- |
| [Delete Remote Share](actions/delete-remote-share.md) | DELETE | Deletes a remote share from Next Cloud OCS. |
| [Get Remote Share](actions/get-remote-share.md) | GET | Retrieves remote share details from Next Cloud OCS. |
| [List Remote Shares](actions/list-remote-shares.md) | GET | Retrieves remote shares from Next Cloud OCS. |

### Richdocuments Document Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Richdocuments Document Link](actions/create-richdocuments-document-link.md) | POST | Creates a new richdocuments document link in Next Cloud OCS. |

### Richdocuments Share Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Richdocuments Share Link](actions/create-richdocuments-share-link.md) | POST | Creates a new richdocuments share link in Next Cloud OCS. |

### Share

| Action | Method | Description |
| --- | --- | --- |
| [Create Share](actions/create-share.md) | POST | Creates a new share in Next Cloud OCS. |
| [Delete Share](actions/delete-share.md) | DELETE | Deletes a share from Next Cloud OCS. |
| [Get Share](actions/get-share.md) | GET | Retrieves share details from Next Cloud OCS. |
| [List Shares](actions/list-shares.md) | GET | Retrieves shares from Next Cloud OCS. |
| [Update Share](actions/update-share.md) | PUT | Updates a share in Next Cloud OCS. |

### Share Email

| Action | Method | Description |
| --- | --- | --- |
| [Send Share Email](actions/send-share-email.md) | POST | Sends a share email in Next Cloud OCS. |

### Sharee

| Action | Method | Description |
| --- | --- | --- |
| [Search Sharees](actions/search-sharees.md) | GET | Finds sharees in Next Cloud OCS. |

### Status Message

| Action | Method | Description |
| --- | --- | --- |
| [Clear Status Message](actions/clear-status-message.md) | DELETE | Clears a status message in Next Cloud OCS. |
| [Set Custom Status Message](actions/set-custom-status-message.md) | PUT | Sets custom status message in Next Cloud OCS. |

### Subadmin Group

| Action | Method | Description |
| --- | --- | --- |
| [Add User Subadmin](actions/add-user-subadmin.md) | POST | Adds a user subadmin in Next Cloud OCS. |
| [List User Subadmins](actions/list-user-subadmins.md) | GET | Retrieves user subadmins from Next Cloud OCS. |
| [Remove User Subadmin](actions/remove-user-subadmin.md) | DELETE | Removes a user subadmin from Next Cloud OCS. |

### Talk Avatar

| Action | Method | Description |
| --- | --- | --- |
| [Delete Talk Conversation Avatar](actions/delete-talk-conversation-avatar.md) | DELETE | Deletes a talk conversation avatar from Next Cloud OCS. |
| [Get Dark Talk Conversation Avatar](actions/get-dark-talk-conversation-avatar.md) | GET | Retrieves the dark talk conversation avatar from Next Cloud OCS. |
| [Get Dark Talk Proxy User Avatar](actions/get-dark-talk-proxy-user-avatar.md) | GET | Retrieves the dark talk proxy user avatar from Next Cloud OCS. |
| [Get Talk Conversation Avatar](actions/get-talk-conversation-avatar.md) | GET | Retrieves talk conversation avatar from Next Cloud OCS. |
| [Get Talk Proxy User Avatar](actions/get-talk-proxy-user-avatar.md) | GET | Retrieves talk proxy user avatar from Next Cloud OCS. |
| [Set Talk Conversation Emoji Avatar](actions/set-talk-conversation-emoji-avatar.md) | PUT | Sets a talk conversation emoji avatar in Next Cloud OCS. |
| [Upload Talk Conversation Avatar](actions/upload-talk-conversation-avatar.md) | PUT | Uploads a talk conversation avatar to Next Cloud OCS. |

### Talk Bot

| Action | Method | Description |
| --- | --- | --- |
| [Disable Talk Bot](actions/disable-talk-bot.md) | PUT | Disables a talk bot in Next Cloud OCS. |
| [Enable Talk Bot](actions/enable-talk-bot.md) | PUT | Enables a talk bot in Next Cloud OCS. |
| [List Talk Bots](actions/list-talk-bots.md) | GET | Retrieves talk bots from Next Cloud OCS. |
| [List Talk Bots Admin](actions/list-talk-bots-admin.md) | GET | Retrieves talk bots admin from Next Cloud OCS. |

### Talk Bot Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Talk Bot Message](actions/send-talk-bot-message.md) | POST | Sends a talk bot message in Next Cloud OCS. |

### Talk Bot Reaction

| Action | Method | Description |
| --- | --- | --- |
| [Add Talk Bot Reaction](actions/add-talk-bot-reaction.md) | POST | Adds a talk bot reaction in Next Cloud OCS. |
| [Delete Talk Bot Reaction](actions/delete-talk-bot-reaction.md) | DELETE | Deletes a talk bot reaction from Next Cloud OCS. |

### Talk Breakout Assistance

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Talk Breakout Assistance](actions/cancel-talk-breakout-assistance.md) | DELETE | Cancels a talk breakout assistance in Next Cloud OCS. |
| [Request Talk Breakout Assistance](actions/request-talk-breakout-assistance.md) | POST | Requests a talk breakout assistance from Next Cloud OCS. |

### Talk Breakout Attendee

| Action | Method | Description |
| --- | --- | --- |
| [Assign Talk Breakout Attendees](actions/assign-talk-breakout-attendees.md) | PUT | Assigns attendees to talk breakout rooms in Next Cloud OCS. |

### Talk Breakout Broadcast

| Action | Method | Description |
| --- | --- | --- |
| [Broadcast To Talk Breakout Rooms](actions/broadcast-to-talk-breakout-rooms.md) | POST | Broadcasts to talk breakout rooms in Next Cloud OCS. |

### Talk Breakout Room

| Action | Method | Description |
| --- | --- | --- |
| [Configure Talk Breakout Rooms](actions/configure-talk-breakout-rooms.md) | POST | Configures talk breakout rooms in Next Cloud OCS. |
| [List Talk Breakout Rooms](actions/list-talk-breakout-rooms.md) | GET | Retrieves talk breakout rooms from Next Cloud OCS. |
| [Remove Talk Breakout Rooms](actions/remove-talk-breakout-rooms.md) | DELETE | Removes talk breakout rooms from Next Cloud OCS. |
| [Start Talk Breakout Rooms](actions/start-talk-breakout-rooms.md) | POST | Starts talk breakout rooms in Next Cloud OCS. |
| [Stop Talk Breakout Rooms](actions/stop-talk-breakout-rooms.md) | DELETE | Stops talk breakout rooms in Next Cloud OCS. |
| [Switch Talk Breakout Room](actions/switch-talk-breakout-room.md) | PUT | Switches talk breakout rooms in Next Cloud OCS. |

### Talk Call

| Action | Method | Description |
| --- | --- | --- |
| [Join Talk Call](actions/join-talk-call.md) | POST | Joins a talk call in Next Cloud OCS. |
| [Leave Talk Call](actions/leave-talk-call.md) | DELETE | Leaves a talk call in Next Cloud OCS. |
| [Ring Talk Call Attendee](actions/ring-talk-call-attendee.md) | POST | Rings a talk call attendee in Next Cloud OCS. |
| [Start Talk Dial Out](actions/start-talk-dial-out.md) | POST | Starts a talk dial-out in Next Cloud OCS. |
| [Update Talk Call Flags](actions/update-talk-call-flags.md) | PUT | Updates talk call flags in Next Cloud OCS. |

### Talk Call Participant

| Action | Method | Description |
| --- | --- | --- |
| [List Talk Call Participants](actions/list-talk-call-participants.md) | GET | Retrieves talk call participants from Next Cloud OCS. |

### Talk Capabilities

| Action | Method | Description |
| --- | --- | --- |
| [Get Talk Conversation Capabilities](actions/get-talk-conversation-capabilities.md) | GET | Retrieves talk conversation capabilities from Next Cloud OCS. |

### Talk Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Allow Talk Guests](actions/allow-talk-guests.md) | PUT | Allows talk guests in Next Cloud OCS. |
| [Create Talk Conversation](actions/create-talk-conversation.md) | POST | Creates a new talk conversation in Next Cloud OCS. |
| [Delete Talk Conversation](actions/delete-talk-conversation.md) | DELETE | Deletes a talk conversation from Next Cloud OCS. |
| [Disallow Talk Guests](actions/disallow-talk-guests.md) | PUT | Disallows talk guests in Next Cloud OCS. |
| [Favorite Talk Conversation](actions/favorite-talk-conversation.md) | PUT | Marks a talk conversation as favorite in Next Cloud OCS. |
| [Get Talk Conversation](actions/get-talk-conversation.md) | GET | Retrieves talk conversation from Next Cloud OCS. |
| [Get Talk Note To Self Conversation](actions/get-talk-note-to-self-conversation.md) | GET | Retrieves talk note-to-self conversation from Next Cloud OCS. |
| [List Open Talk Conversations](actions/list-open-talk-conversations.md) | GET | Retrieves open talk conversations from Next Cloud OCS. |
| [List Talk Conversations](actions/list-talk-conversations.md) | GET | Retrieves talk conversations from Next Cloud OCS. |
| [Rename Talk Conversation](actions/rename-talk-conversation.md) | PUT | Renames a talk conversation in Next Cloud OCS. |
| [Set Talk Call Notification Level](actions/set-talk-call-notification-level.md) | PUT | Sets a talk call notification level in Next Cloud OCS. |
| [Set Talk Conversation Description](actions/set-talk-conversation-description.md) | PUT | Sets a talk conversation description in Next Cloud OCS. |
| [Set Talk Listable Scope](actions/set-talk-listable-scope.md) | PUT | Sets a talk listable scope in Next Cloud OCS. |
| [Set Talk Mention Permissions](actions/set-talk-mention-permissions.md) | PUT | Sets talk mention permissions in Next Cloud OCS. |
| [Set Talk Message Expiration](actions/set-talk-message-expiration.md) | PUT | Sets a talk message expiration in Next Cloud OCS. |
| [Set Talk Notification Level](actions/set-talk-notification-level.md) | PUT | Sets a talk notification level in Next Cloud OCS. |
| [Set Talk Password](actions/set-talk-password.md) | PUT | Sets a talk password in Next Cloud OCS. |
| [Set Talk Permissions](actions/set-talk-permissions.md) | PUT | Sets talk permissions in Next Cloud OCS. |
| [Set Talk Read Only](actions/set-talk-read-only.md) | PUT | Sets talk read-only mode in Next Cloud OCS. |
| [Set Talk Recording Consent](actions/set-talk-recording-consent.md) | PUT | Sets a talk recording consent in Next Cloud OCS. |
| [Unfavorite Talk Conversation](actions/unfavorite-talk-conversation.md) | PUT | Removes a talk conversation from favorites in Next Cloud OCS. |

### Talk Dial In

| Action | Method | Description |
| --- | --- | --- |
| [Verify Talk Dial In](actions/verify-talk-dial-in.md) | GET | Verifies talk dial-in details in Next Cloud OCS. |

### Talk Dial Out

| Action | Method | Description |
| --- | --- | --- |
| [Clear Rejected Talk Dial Out](actions/clear-rejected-talk-dial-out.md) | DELETE | Clears a rejected talk dial-out in Next Cloud OCS. |
| [Verify Talk Dial Out](actions/verify-talk-dial-out.md) | GET | Verifies talk dial-out details in Next Cloud OCS. |

### Talk File Integration

| Action | Method | Description |
| --- | --- | --- |
| [Get Talk File Integration](actions/get-talk-file-integration.md) | GET | Retrieves talk file integration from Next Cloud OCS. |

### Talk Guest

| Action | Method | Description |
| --- | --- | --- |
| [Set Talk Guest Name](actions/set-talk-guest-name.md) | PUT | Sets a talk guest name in Next Cloud OCS. |

### Talk Invitation

| Action | Method | Description |
| --- | --- | --- |
| [Resend Talk Invitations](actions/resend-talk-invitations.md) | POST | Resends talk invitations in Next Cloud OCS. |

### Talk Mention

| Action | Method | Description |
| --- | --- | --- |
| [List Talk Mentions](actions/list-talk-mentions.md) | GET | Retrieves talk mentions from Next Cloud OCS. |

### Talk Message

| Action | Method | Description |
| --- | --- | --- |
| [Clear Talk Chat History](actions/clear-talk-chat-history.md) | DELETE | Clears a talk chat history in Next Cloud OCS. |
| [Delete Talk Chat Message](actions/delete-talk-chat-message.md) | DELETE | Deletes a talk chat message from Next Cloud OCS. |
| [Edit Talk Chat Message](actions/edit-talk-chat-message.md) | PUT | Edits a talk chat message in Next Cloud OCS. |
| [Get Talk Chat Message Context](actions/get-talk-chat-message-context.md) | GET | Retrieves talk chat message context from Next Cloud OCS. |
| [List Talk Chat Messages](actions/list-talk-chat-messages.md) | GET | Retrieves talk chat messages from Next Cloud OCS. |
| [Mark Talk Chat Read](actions/mark-talk-chat-read.md) | PUT | Marks talk chat as read in Next Cloud OCS. |
| [Mark Talk Chat Unread](actions/mark-talk-chat-unread.md) | PUT | Marks talk chat as unread in Next Cloud OCS. |
| [Send Talk Chat Message](actions/send-talk-chat-message.md) | POST | Sends a talk chat message in Next Cloud OCS. |
| [Share File To Talk Chat](actions/share-file-to-talk-chat.md) | POST | Shares a file to talk chat in Next Cloud OCS. |

### Talk Participant

| Action | Method | Description |
| --- | --- | --- |
| [Add Active Talk Participant](actions/add-active-talk-participant.md) | POST | Adds an active talk participant in Next Cloud OCS. |
| [Add Talk Participant](actions/add-talk-participant.md) | POST | Adds a talk participant in Next Cloud OCS. |
| [Demote Talk Moderator](actions/demote-talk-moderator.md) | PUT | Demotes a talk moderator in Next Cloud OCS. |
| [Get Talk Dial In Participant](actions/get-talk-dial-in-participant.md) | GET | Retrieves talk dial-in participant from Next Cloud OCS. |
| [Leave Talk Conversation](actions/leave-talk-conversation.md) | DELETE | Leaves a talk conversation in Next Cloud OCS. |
| [List Talk Breakout Participants](actions/list-talk-breakout-participants.md) | GET | Retrieves talk breakout participants from Next Cloud OCS. |
| [List Talk Participants](actions/list-talk-participants.md) | GET | Retrieves talk participants from Next Cloud OCS. |
| [Promote Talk Moderator](actions/promote-talk-moderator.md) | PUT | Promotes a talk moderator in Next Cloud OCS. |
| [Remove Active Talk Participant](actions/remove-active-talk-participant.md) | DELETE | Removes an active talk participant from Next Cloud OCS. |
| [Remove Talk Attendee](actions/remove-talk-attendee.md) | DELETE | Removes a talk attendee from Next Cloud OCS. |
| [Set All Talk Attendee Permissions](actions/set-all-talk-attendee-permissions.md) | PUT | Sets all talk attendee permissions in Next Cloud OCS. |
| [Set Talk Attendee Permissions](actions/set-talk-attendee-permissions.md) | PUT | Sets talk attendee permissions in Next Cloud OCS. |
| [Set Talk Participant State](actions/set-talk-participant-state.md) | PUT | Sets a talk participant state in Next Cloud OCS. |

### Talk Poll

| Action | Method | Description |
| --- | --- | --- |
| [Create Talk Poll](actions/create-talk-poll.md) | POST | Creates a new talk poll in Next Cloud OCS. |
| [Delete Talk Poll](actions/delete-talk-poll.md) | DELETE | Deletes a talk poll from Next Cloud OCS. |
| [Get Talk Poll](actions/get-talk-poll.md) | GET | Retrieves talk poll from Next Cloud OCS. |
| [Update Talk Draft Poll](actions/update-talk-draft-poll.md) | PUT | Updates a talk draft poll in Next Cloud OCS. |
| [Vote Talk Poll](actions/vote-talk-poll.md) | PUT | Votes on a talk poll in Next Cloud OCS. |

### Talk Public Share Auth

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate Talk Public Share](actions/authenticate-talk-public-share.md) | POST | Authenticates a talk public share in Next Cloud OCS. |

### Talk Public Share Integration

| Action | Method | Description |
| --- | --- | --- |
| [Get Talk Public Share Integration](actions/get-talk-public-share-integration.md) | GET | Retrieves talk public share integration from Next Cloud OCS. |

### Talk Reaction

| Action | Method | Description |
| --- | --- | --- |
| [Add Talk Message Reaction](actions/add-talk-message-reaction.md) | POST | Adds a talk message reaction in Next Cloud OCS. |
| [Delete Talk Message Reaction](actions/delete-talk-message-reaction.md) | DELETE | Deletes a talk message reaction from Next Cloud OCS. |
| [List Talk Message Reactions](actions/list-talk-message-reactions.md) | GET | Retrieves talk message reactions from Next Cloud OCS. |

### Talk Recording

| Action | Method | Description |
| --- | --- | --- |
| [Start Talk Recording](actions/start-talk-recording.md) | POST | Starts a talk recording in Next Cloud OCS. |
| [Stop Talk Recording](actions/stop-talk-recording.md) | DELETE | Stops a talk recording in Next Cloud OCS. |
| [Store Talk Recording](actions/store-talk-recording.md) | POST | Stores a talk recording in Next Cloud OCS. |

### Talk Recording Backend

| Action | Method | Description |
| --- | --- | --- |
| [Register Talk Recording Backend](actions/register-talk-recording-backend.md) | POST | Registers a talk recording backend in Next Cloud OCS. |

### Talk Recording Notification

| Action | Method | Description |
| --- | --- | --- |
| [Delete Talk Recording Notification](actions/delete-talk-recording-notification.md) | DELETE | Deletes a talk recording notification from Next Cloud OCS. |

### Talk Recording Share

| Action | Method | Description |
| --- | --- | --- |
| [Share Talk Recording To Chat](actions/share-talk-recording-to-chat.md) | POST | Shares talk recording to chat in Next Cloud OCS. |

### Talk Reminder

| Action | Method | Description |
| --- | --- | --- |
| [Create Talk Message Reminder](actions/create-talk-message-reminder.md) | POST | Creates a new talk message reminder in Next Cloud OCS. |
| [Delete Talk Message Reminder](actions/delete-talk-message-reminder.md) | DELETE | Deletes a talk message reminder from Next Cloud OCS. |
| [Get Talk Message Reminder](actions/get-talk-message-reminder.md) | GET | Retrieves talk message reminder from Next Cloud OCS. |

### Talk Settings

| Action | Method | Description |
| --- | --- | --- |
| [Update Talk Sip Settings](actions/update-talk-sip-settings.md) | PUT | Updates a talk sip settings in Next Cloud OCS. |
| [Update Talk User Settings](actions/update-talk-user-settings.md) | PUT | Updates a talk user settings in Next Cloud OCS. |

### Talk Shared Item

| Action | Method | Description |
| --- | --- | --- |
| [List Talk Shared Items](actions/list-talk-shared-items.md) | GET | Retrieves talk shared items from Next Cloud OCS. |
| [List Talk Shared Items Overview](actions/list-talk-shared-items-overview.md) | GET | Retrieves talk shared items overview from Next Cloud OCS. |

### Talk Webinar

| Action | Method | Description |
| --- | --- | --- |
| [Set Talk Webinar Lobby](actions/set-talk-webinar-lobby.md) | PUT | Sets a talk webinar lobby in Next Cloud OCS. |
| [Set Talk Webinar Sip](actions/set-talk-webinar-sip.md) | PUT | Sets a talk webinar sip in Next Cloud OCS. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Accept Cloud Share](actions/accept-cloud-share.md) | PUT | Accepts a cloud share in Next Cloud OCS. |
| [Accept File Ownership Transfer](actions/accept-file-ownership-transfer.md) | PUT | Accepts a file ownership transfer in Next Cloud OCS. |
| [Accept Pending Share](actions/accept-pending-share.md) | PUT | Accepts a pending share in Next Cloud OCS. |
| [Activate Web Push Device](actions/activate-web-push-device.md) | PUT | Activates a web push device in Next Cloud OCS. |
| [Add Resource To Collaboration Collection](actions/add-resource-to-collaboration-collection.md) | POST | Adds resource to collaboration collection in Next Cloud OCS. |
| [Cancel Consumer Task](actions/cancel-consumer-task.md) | PUT | Cancels a consumer task in Next Cloud OCS. |
| [Cancel Task Processing Task](actions/cancel-task-processing-task.md) | PUT | Cancels a task processing task in Next Cloud OCS. |
| [Check Text To Image Availability](actions/check-text-to-image-availability.md) | GET | Checks text-to-image availability in Next Cloud OCS. |
| [Clear LDAP Wizard Mappings](actions/clear-ldap-wizard-mappings.md) | PUT | Clears LDAP wizard mappings in Next Cloud OCS. |
| [Confirm App Password](actions/confirm-app-password.md) | PUT | Confirms an app password in Next Cloud OCS. |
| [Convert File](actions/convert-file.md) | POST | Converts a file in Next Cloud OCS. |
| [Copy LDAP Config](actions/copy-ldap-config.md) | POST | Copies a LDAP config in Next Cloud OCS. |
| [Create Admin Notification V3](actions/create-admin-notification-v3.md) | POST | Creates an new admin notification in Next Cloud OCS. |
| [Create Cloud Group V2](actions/create-cloud-group-v2.md) | POST | Creates a new cloud group in Next Cloud OCS. |
| [Create Cloud Share](actions/create-cloud-share.md) | POST | Creates a new cloud share in Next Cloud OCS. |
| [Create Cloud User V2](actions/create-cloud-user-v2.md) | POST | Creates a new cloud user in Next Cloud OCS. |
| [Create Collaboration Resource](actions/create-collaboration-resource.md) | POST | Creates a new collaboration resource in Next Cloud OCS. |
| [Create File From Template](actions/create-file-from-template.md) | POST | Creates new file from template in Next Cloud OCS. |
| [Create Global Workflow](actions/create-global-workflow.md) | POST | Creates a new global workflow in Next Cloud OCS. |
| [Create LDAP Config](actions/create-ldap-config.md) | POST | Creates a new LDAP config in Next Cloud OCS. |
| [Create Trusted Server](actions/create-trusted-server.md) | POST | Creates a new trusted server in Next Cloud OCS. |
| [Create User Workflow](actions/create-user-workflow.md) | POST | Creates a new user workflow in Next Cloud OCS. |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Next Cloud OCS. |
| [Decline Cloud Share](actions/decline-cloud-share.md) | PUT | Declines a cloud share in Next Cloud OCS. |
| [Delete App Config Value](actions/delete-app-config-value.md) | DELETE | Deletes an app config value from Next Cloud OCS. |
| [Delete App Password](actions/delete-app-password.md) | DELETE | Deletes an app password from Next Cloud OCS. |
| [Delete App Webhooks](actions/delete-app-webhooks.md) | DELETE | Deletes app webhooks from Next Cloud OCS. |
| [Delete Cloud Group V2](actions/delete-cloud-group-v2.md) | DELETE | Deletes a cloud group from Next Cloud OCS. |
| [Delete Cloud User V2](actions/delete-cloud-user-v2.md) | DELETE | Deletes a cloud user from Next Cloud OCS. |
| [Delete Collaboration Collection](actions/delete-collaboration-collection.md) | DELETE | Deletes a collaboration collection from Next Cloud OCS. |
| [Delete Consumer Task](actions/delete-consumer-task.md) | DELETE | Deletes a consumer task from Next Cloud OCS. |
| [Delete File Ownership Transfer](actions/delete-file-ownership-transfer.md) | DELETE | Deletes a file ownership transfer from Next Cloud OCS. |
| [Delete File Reminder](actions/delete-file-reminder.md) | DELETE | Deletes a file reminder from Next Cloud OCS. |
| [Delete Global Workflow](actions/delete-global-workflow.md) | DELETE | Deletes a global workflow from Next Cloud OCS. |
| [Delete LDAP Config](actions/delete-ldap-config.md) | DELETE | Deletes a LDAP config from Next Cloud OCS. |
| [Delete Task Processing Task](actions/delete-task-processing-task.md) | DELETE | Deletes a task processing task from Next Cloud OCS. |
| [Delete Text Processing Task](actions/delete-text-processing-task.md) | DELETE | Deletes a text processing task from Next Cloud OCS. |
| [Delete Text To Image Task](actions/delete-text-to-image-task.md) | DELETE | Deletes text to image task from Next Cloud OCS. |
| [Delete Theming Theme](actions/delete-theming-theme.md) | DELETE | Deletes a theming theme from Next Cloud OCS. |
| [Delete Trusted Server](actions/delete-trusted-server.md) | DELETE | Deletes a trusted server from Next Cloud OCS. |
| [Delete User Workflow](actions/delete-user-workflow.md) | DELETE | Deletes a user workflow from Next Cloud OCS. |
| [Delete Web Push Device](actions/delete-web-push-device.md) | DELETE | Deletes a web push device from Next Cloud OCS. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from Next Cloud OCS. |
| [Disable Cloud App V2](actions/disable-cloud-app-v2.md) | DELETE | Disables a cloud app in Next Cloud OCS. |
| [Disable Cloud User V2](actions/disable-cloud-user-v2.md) | PUT | Disables a cloud user in Next Cloud OCS. |
| [Disable Two Factor Provider](actions/disable-two-factor-provider.md) | PUT | Disables a two factor provider in Next Cloud OCS. |
| [Enable Cloud App V2](actions/enable-cloud-app-v2.md) | PUT | Enables a cloud app in Next Cloud OCS. |
| [Enable Cloud User V2](actions/enable-cloud-user-v2.md) | PUT | Enables a cloud user in Next Cloud OCS. |
| [Enable Theming Theme](actions/enable-theming-theme.md) | PUT | Enables a theming theme in Next Cloud OCS. |
| [Enable Two Factor Provider](actions/enable-two-factor-provider.md) | PUT | Enables a two factor provider in Next Cloud OCS. |
| [Extract Public References](actions/extract-public-references.md) | POST | Extracts public references in Next Cloud OCS. |
| [Extract References](actions/extract-references.md) | POST | Extracts references in Next Cloud OCS. |
| [Get App Config Value](actions/get-app-config-value.md) | GET | Retrieves app config value from Next Cloud OCS. |
| [Get App Password](actions/get-app-password.md) | GET | Retrieves app password from Next Cloud OCS. |
| [Get Cloud App V2](actions/get-cloud-app-v2.md) | GET | Retrieves cloud app from Next Cloud OCS. |
| [Get Cloud Capabilities V2](actions/get-cloud-capabilities-v2.md) | GET | Retrieves cloud capabilities from Next Cloud OCS. |
| [Get Cloud Group V2](actions/get-cloud-group-v2.md) | GET | Retrieves cloud group from Next Cloud OCS. |
| [Get Cloud Shared Secret](actions/get-cloud-shared-secret.md) | GET | Retrieves cloud shared secret from Next Cloud OCS. |
| [Get Cloud User V2](actions/get-cloud-user-v2.md) | GET | Retrieves cloud user from Next Cloud OCS. |
| [Get Collaboration Collection](actions/get-collaboration-collection.md) | GET | Retrieves collaboration collection from Next Cloud OCS. |
| [Get Collaboration Resource](actions/get-collaboration-resource.md) | GET | Retrieves collaboration resource from Next Cloud OCS. |
| [Get Consumer Task](actions/get-consumer-task.md) | GET | Retrieves consumer task from Next Cloud OCS. |
| [Get Current Cloud User V2](actions/get-current-cloud-user-v2.md) | GET | Retrieves the current cloud user from Next Cloud OCS. |
| [Get Dashboard Layout](actions/get-dashboard-layout.md) | GET | Retrieves dashboard layout from Next Cloud OCS. |
| [Get Federation Shared Secret](actions/get-federation-shared-secret.md) | GET | Retrieves federation shared secret from Next Cloud OCS. |
| [Get File Reminder](actions/get-file-reminder.md) | GET | Retrieves file reminder from Next Cloud OCS. |
| [Get File Template Fields](actions/get-file-template-fields.md) | GET | Retrieves file template fields from Next Cloud OCS. |
| [Get Global Workflow](actions/get-global-workflow.md) | GET | Retrieves global workflow from Next Cloud OCS. |
| [Get Hovercard](actions/get-hovercard.md) | GET | Retrieves hovercard from Next Cloud OCS. |
| [Get Instance Status](actions/get-instance-status.md) | GET | Retrieves instance status from Next Cloud OCS. |
| [Get LDAP Config](actions/get-ldap-config.md) | GET | Retrieves LDAP config from Next Cloud OCS. |
| [Get Next Provider Task](actions/get-next-provider-task.md) | GET | Retrieves next provider task from Next Cloud OCS. |
| [Get Next Provider Task Batch](actions/get-next-provider-task-batch.md) | GET | Retrieves next provider task batch from Next Cloud OCS. |
| [Get One Time App Password](actions/get-one-time-app-password.md) | GET | Retrieves one time app password from Next Cloud OCS. |
| [Get Profile](actions/get-profile.md) | GET | Retrieves profile from Next Cloud OCS. |
| [Get Provider Task File](actions/get-provider-task-file.md) | GET | Retrieves provider task file from Next Cloud OCS. |
| [Get Share Token](actions/get-share-token.md) | GET | Retrieves share token from Next Cloud OCS. |
| [Get Task Processing Queue Stats](actions/get-task-processing-queue-stats.md) | GET | Retrieves task processing queue stats from Next Cloud OCS. |
| [Get Task Processing Task](actions/get-task-processing-task.md) | GET | Retrieves task processing task from Next Cloud OCS. |
| [Get Task Processing Task File](actions/get-task-processing-task-file.md) | GET | Retrieves task processing task file from Next Cloud OCS. |
| [Get Team Resource](actions/get-team-resource.md) | GET | Retrieves team resource from Next Cloud OCS. |
| [Get Templates Path](actions/get-templates-path.md) | POST | Retrieves templates path from Next Cloud OCS. |
| [Get Text Processing Task](actions/get-text-processing-task.md) | GET | Retrieves text processing task from Next Cloud OCS. |
| [Get Text To Image Result Image](actions/get-text-to-image-result-image.md) | GET | Retrieves text to image result image from Next Cloud OCS. |
| [Get Text To Image Task](actions/get-text-to-image-task.md) | GET | Retrieves text to image task from Next Cloud OCS. |
| [Get Two Factor State](actions/get-two-factor-state.md) | GET | Retrieves two factor state from Next Cloud OCS. |
| [Get Update App Changelog](actions/get-update-app-changelog.md) | GET | Retrieves update app changelog from Next Cloud OCS. |
| [Get Update App List](actions/get-update-app-list.md) | GET | Retrieves update app list from Next Cloud OCS. |
| [Get User Editable Fields](actions/get-user-editable-fields.md) | GET | Retrieves user editable fields from Next Cloud OCS. |
| [Get User Groups Details](actions/get-user-groups-details.md) | GET | Retrieves user groups details from Next Cloud OCS. |
| [Get User Subadmins Details](actions/get-user-subadmins-details.md) | GET | Retrieves user subadmins details from Next Cloud OCS. |
| [Get User Workflow](actions/get-user-workflow.md) | GET | Retrieves user workflow from Next Cloud OCS. |
| [Get Weather Forecast](actions/get-weather-forecast.md) | GET | Retrieves weather forecast from Next Cloud OCS. |
| [Get Web Push Vapid Key](actions/get-web-push-vapid-key.md) | GET | Retrieves web push vapid key from Next Cloud OCS. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves webhook from Next Cloud OCS. |
| [List App Config Apps](actions/list-app-config-apps.md) | GET | Retrieves app config apps from Next Cloud OCS. |
| [List App Config Keys](actions/list-app-config-keys.md) | GET | Retrieves app config keys from Next Cloud OCS. |
| [List Cloud Apps V2](actions/list-cloud-apps-v2.md) | GET | Retrieves cloud apps from Next Cloud OCS. |
| [List Cloud Groups V2](actions/list-cloud-groups-v2.md) | GET | Retrieves cloud groups from Next Cloud OCS. |
| [List Cloud Users V2](actions/list-cloud-users-v2.md) | GET | Retrieves cloud users from Next Cloud OCS. |
| [List Consumer Task Types](actions/list-consumer-task-types.md) | GET | Retrieves consumer task types from Next Cloud OCS. |
| [List Current User Apps](actions/list-current-user-apps.md) | GET | Retrieves the current user apps from Next Cloud OCS. |
| [List Dashboard Statuses](actions/list-dashboard-statuses.md) | GET | Retrieves dashboard statuses from Next Cloud OCS. |
| [List Dashboard Widget Items](actions/list-dashboard-widget-items.md) | GET | Retrieves dashboard widget items from Next Cloud OCS. |
| [List Dashboard Widget Items V2](actions/list-dashboard-widget-items-v2.md) | GET | Retrieves dashboard widget items from Next Cloud OCS. |
| [List Dashboard Widgets](actions/list-dashboard-widgets.md) | GET | Retrieves dashboard widgets from Next Cloud OCS. |
| [List Declarative Setting Forms](actions/list-declarative-setting-forms.md) | GET | Retrieves declarative setting forms from Next Cloud OCS. |
| [List Deleted Shares](actions/list-deleted-shares.md) | GET | Retrieves deleted shares from Next Cloud OCS. |
| [List Direct Editing Templates](actions/list-direct-editing-templates.md) | GET | Retrieves direct editing templates from Next Cloud OCS. |
| [List Disabled Users](actions/list-disabled-users.md) | GET | Retrieves disabled users from Next Cloud OCS. |
| [List External Mounts](actions/list-external-mounts.md) | GET | Retrieves external mounts from Next Cloud OCS. |
| [List File Templates](actions/list-file-templates.md) | GET | Retrieves file templates from Next Cloud OCS. |
| [List Folder Tree](actions/list-folder-tree.md) | GET | Retrieves folder tree from Next Cloud OCS. |
| [List Global Workflows](actions/list-global-workflows.md) | GET | Retrieves global workflows from Next Cloud OCS. |
| [List Group Subadmins](actions/list-group-subadmins.md) | GET | Retrieves group subadmins from Next Cloud OCS. |
| [List Group Users](actions/list-group-users.md) | GET | Retrieves group users from Next Cloud OCS. |
| [List Group Users Details](actions/list-group-users-details.md) | GET | Retrieves group users details from Next Cloud OCS. |
| [List Groups Details](actions/list-groups-details.md) | GET | Retrieves groups details from Next Cloud OCS. |
| [List Navigation Apps](actions/list-navigation-apps.md) | GET | Retrieves navigation apps from Next Cloud OCS. |
| [List Navigation Settings](actions/list-navigation-settings.md) | GET | Retrieves navigation settings from Next Cloud OCS. |
| [List Recent Users](actions/list-recent-users.md) | GET | Retrieves the recent users from Next Cloud OCS. |
| [List Reference Providers](actions/list-reference-providers.md) | GET | Retrieves reference providers from Next Cloud OCS. |
| [List Search Providers](actions/list-search-providers.md) | GET | Retrieves search providers from Next Cloud OCS. |
| [List Sharee Recommendations V2](actions/list-sharee-recommendations-v2.md) | GET | Retrieves sharee recommendations from Next Cloud OCS. |
| [List Task Processing Task Types](actions/list-task-processing-task-types.md) | GET | Retrieves task processing task types from Next Cloud OCS. |
| [List Task Processing Tasks](actions/list-task-processing-tasks.md) | GET | Retrieves task processing tasks from Next Cloud OCS. |
| [List Task Processing Tasks By App](actions/list-task-processing-tasks-by-app.md) | GET | Retrieves task processing tasks by app from Next Cloud OCS. |
| [List Team Resources](actions/list-team-resources.md) | GET | Retrieves team resources from Next Cloud OCS. |
| [List Text Processing Task Types](actions/list-text-processing-task-types.md) | GET | Retrieves text processing task types from Next Cloud OCS. |
| [List Text Processing Tasks By App](actions/list-text-processing-tasks-by-app.md) | GET | Retrieves text processing tasks by app from Next Cloud OCS. |
| [List Text To Image Tasks By App](actions/list-text-to-image-tasks-by-app.md) | GET | Retrieves text to image tasks by app from Next Cloud OCS. |
| [List Translation Languages](actions/list-translation-languages.md) | GET | Retrieves translation languages from Next Cloud OCS. |
| [List Trusted Servers](actions/list-trusted-servers.md) | GET | Retrieves trusted servers from Next Cloud OCS. |
| [List Upcoming Calendar Events](actions/list-upcoming-calendar-events.md) | GET | Retrieves the upcoming calendar events from Next Cloud OCS. |
| [List User Workflows](actions/list-user-workflows.md) | GET | Retrieves user workflows from Next Cloud OCS. |
| [List Users Details](actions/list-users-details.md) | GET | Retrieves users details from Next Cloud OCS. |
| [List Weather Favorites](actions/list-weather-favorites.md) | GET | Retrieves weather favorites from Next Cloud OCS. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Next Cloud OCS. |
| [Move Cloud Share](actions/move-cloud-share.md) | PUT | Moves a cloud share in Next Cloud OCS. |
| [Open Local Editor](actions/open-local-editor.md) | POST | Opens a local editor in Next Cloud OCS. |
| [Open Local Editor Token](actions/open-local-editor-token.md) | POST | Opens a local editor token in Next Cloud OCS. |
| [Register Web Push Device](actions/register-web-push-device.md) | POST | Registers a web push device in Next Cloud OCS. |
| [Request Cloud Shared Secret](actions/request-cloud-shared-secret.md) | POST | Requests a cloud shared secret from Next Cloud OCS. |
| [Request Federation Shared Secret](actions/request-federation-shared-secret.md) | POST | Requests a federation shared secret from Next Cloud OCS. |
| [Request File Ownership Transfer](actions/request-file-ownership-transfer.md) | POST | Requests a file ownership transfer from Next Cloud OCS. |
| [Reshare Cloud Share](actions/reshare-cloud-share.md) | PUT | Reshares a cloud share in Next Cloud OCS. |
| [Resolve Public Reference](actions/resolve-public-reference.md) | GET | Resolves a public reference in Next Cloud OCS. |
| [Resolve Public Reference With Post](actions/resolve-public-reference-with-post.md) | POST | Resolves a public reference in Next Cloud OCS using POST input. |
| [Resolve Reference](actions/resolve-reference.md) | GET | Resolves a reference in Next Cloud OCS. |
| [Resolve Reference With Post](actions/resolve-reference-with-post.md) | POST | Resolves a reference in Next Cloud OCS using POST input. |
| [Restore Deleted Share](actions/restore-deleted-share.md) | PUT | Restores a deleted share in Next Cloud OCS. |
| [Restore User Status Message](actions/restore-user-status-message.md) | DELETE | Restores a user status message in Next Cloud OCS. |
| [Revoke Cloud Share](actions/revoke-cloud-share.md) | PUT | Revokes a cloud share in Next Cloud OCS. |
| [Rotate App Password](actions/rotate-app-password.md) | POST | Rotates an app password in Next Cloud OCS. |
| [Run LDAP Wizard Action](actions/run-ldap-wizard-action.md) | PUT | Runs a LDAP wizard action in Next Cloud OCS. |
| [Schedule Consumer Task](actions/schedule-consumer-task.md) | POST | Schedules a consumer task in Next Cloud OCS. |
| [Schedule Task Processing Task](actions/schedule-task-processing-task.md) | POST | Schedules a task processing task in Next Cloud OCS. |
| [Schedule Text Processing Task](actions/schedule-text-processing-task.md) | POST | Schedules a text processing task in Next Cloud OCS. |
| [Schedule Text To Image Task](actions/schedule-text-to-image-task.md) | POST | Schedules text to image task in Next Cloud OCS. |
| [Search Collaboration Collections](actions/search-collaboration-collections.md) | GET | Finds collaboration collections in Next Cloud OCS. |
| [Search Provider](actions/search-provider.md) | GET | Finds provider in Next Cloud OCS. |
| [Search Sharees V2](actions/search-sharees-v2.md) | GET | Finds sharees in Next Cloud OCS. |
| [Search Users By Phone](actions/search-users-by-phone.md) | POST | Finds users in Next Cloud OCS by phone number. |
| [Send Test Notification To Self](actions/send-test-notification-to-self.md) | POST | Sends test notification to self in Next Cloud OCS. |
| [Send User Status Heartbeat](actions/send-user-status-heartbeat.md) | PUT | Sends a user status heartbeat in Next Cloud OCS. |
| [Set App Config Value](actions/set-app-config-value.md) | PUT | Sets an app config value in Next Cloud OCS. |
| [Set Cloud Share Permissions](actions/set-cloud-share-permissions.md) | PUT | Sets cloud share permissions in Next Cloud OCS. |
| [Set Declarative Setting Value](actions/set-declarative-setting-value.md) | PUT | Sets a declarative setting value in Next Cloud OCS. |
| [Set File Reminder](actions/set-file-reminder.md) | PUT | Sets a file reminder in Next Cloud OCS. |
| [Set Provider Task Result](actions/set-provider-task-result.md) | PUT | Sets a provider task result in Next Cloud OCS. |
| [Set Reference Provider](actions/set-reference-provider.md) | PUT | Sets a reference provider in Next Cloud OCS. |
| [Set Sensitive Declarative Setting Value](actions/set-sensitive-declarative-setting-value.md) | PUT | Sets a sensitive declarative setting value in Next Cloud OCS. |
| [Test LDAP Config](actions/test-ldap-config.md) | PUT | Tests a LDAP config in Next Cloud OCS. |
| [Translate Text](actions/translate-text.md) | POST | Translates a text in Next Cloud OCS. |
| [Unshare Cloud Share](actions/unshare-cloud-share.md) | PUT | Unshares a cloud share in Next Cloud OCS. |
| [Update Admin Notification Settings](actions/update-admin-notification-settings.md) | PUT | Updates an admin notification settings in Next Cloud OCS. |
| [Update Cloud User V2](actions/update-cloud-user-v2.md) | PUT | Updates a cloud user in Next Cloud OCS. |
| [Update Collaboration Collection](actions/update-collaboration-collection.md) | PUT | Updates a collaboration collection in Next Cloud OCS. |
| [Update Dashboard Layout](actions/update-dashboard-layout.md) | PUT | Updates a dashboard layout in Next Cloud OCS. |
| [Update Dashboard Statuses](actions/update-dashboard-statuses.md) | PUT | Updates dashboard statuses in Next Cloud OCS. |
| [Update Global Workflow](actions/update-global-workflow.md) | PUT | Updates a global workflow in Next Cloud OCS. |
| [Update Group](actions/update-group.md) | PUT | Updates a group in Next Cloud OCS. |
| [Update LDAP Config](actions/update-ldap-config.md) | PUT | Updates a LDAP config in Next Cloud OCS. |
| [Update Notification Settings](actions/update-notification-settings.md) | PUT | Updates a notification settings in Next Cloud OCS. |
| [Update Profile](actions/update-profile.md) | PUT | Updates a profile in Next Cloud OCS. |
| [Update Provider Task Progress](actions/update-provider-task-progress.md) | PUT | Updates a provider task progress in Next Cloud OCS. |
| [Update User Collection](actions/update-user-collection.md) | PUT | Updates a user collection in Next Cloud OCS. |
| [Update User Workflow](actions/update-user-workflow.md) | PUT | Updates a user workflow in Next Cloud OCS. |
| [Update Weather Favorites](actions/update-weather-favorites.md) | PUT | Updates weather favorites in Next Cloud OCS. |
| [Update Weather Location](actions/update-weather-location.md) | PUT | Updates a weather location in Next Cloud OCS. |
| [Update Weather Mode](actions/update-weather-mode.md) | PUT | Updates a weather mode in Next Cloud OCS. |
| [Update Weather Personal Data Use](actions/update-weather-personal-data-use.md) | PUT | Updates a weather personal data use in Next Cloud OCS. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates a webhook in Next Cloud OCS. |
| [Upload Provider Task File](actions/upload-provider-task-file.md) | POST | Uploads a provider task file to Next Cloud OCS. |
| [Wipe User Devices](actions/wipe-user-devices.md) | PUT | Wipes user devices in Next Cloud OCS. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in Next Cloud OCS. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes a user from Next Cloud OCS. |
| [Disable User](actions/disable-user.md) | PUT | Disables a user in Next Cloud OCS. |
| [Enable User](actions/enable-user.md) | PUT | Enables a user in Next Cloud OCS. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Next Cloud OCS. |
| [Resend User Welcome Email](actions/resend-user-welcome-email.md) | POST | Resends a user welcome email in Next Cloud OCS. |
| [Update User Field](actions/update-user-field.md) | PUT | Updates a user field in Next Cloud OCS. |

### User Group

| Action | Method | Description |
| --- | --- | --- |
| [Add User To Group](actions/add-user-to-group.md) | POST | Adds a user to a group in Next Cloud OCS. |
| [Get User Groups](actions/get-user-groups.md) | GET | Retrieves user groups from Next Cloud OCS. |
| [Remove User From Group](actions/remove-user-from-group.md) | DELETE | Removes a user from a group in Next Cloud OCS. |

### User Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get User Metadata](actions/get-user-metadata.md) | GET | Retrieves user metadata from Next Cloud OCS. |

### User Preference

| Action | Method | Description |
| --- | --- | --- |
| [Delete User Preference](actions/delete-user-preference.md) | DELETE | Deletes a user preference from Next Cloud OCS. |
| [Set User Preference](actions/set-user-preference.md) | PUT | Sets a user preference in Next Cloud OCS. |

### User Preferences

| Action | Method | Description |
| --- | --- | --- |
| [Delete User Preferences](actions/delete-user-preferences.md) | DELETE | Deletes user preferences from Next Cloud OCS. |
| [Set User Preferences](actions/set-user-preferences.md) | PUT | Sets user preferences in Next Cloud OCS. |

### User Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Backup User Status](actions/get-backup-user-status.md) | GET | Retrieves backup user status from Next Cloud OCS. |
| [Get Own Status](actions/get-own-status.md) | GET | Retrieves your status from Next Cloud OCS. |
| [Get User Status](actions/get-user-status.md) | GET | Retrieves user status from Next Cloud OCS. |
| [List User Statuses](actions/list-user-statuses.md) | GET | Retrieves user statuses from Next Cloud OCS. |
| [Set Own Status](actions/set-own-status.md) | PUT | Sets your status in Next Cloud OCS. |
| [Set Predefined Status Message](actions/set-predefined-status-message.md) | PUT | Sets a predefined status message in Next Cloud OCS. |

### Weather Location

| Action | Method | Description |
| --- | --- | --- |
| [Get Weather Location](actions/get-weather-location.md) | GET | Retrieves weather location from Next Cloud OCS. |

