# Zoom Team Chat: Native API Reference

A consolidated summary of Zoom Team Chat's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developers.zoom.us/docs/api/rest/reference/chat/methods/
- **API base URL:** `https://api.zoom.us/v2`

## Authentication

### OAuth2

Use a Zoom General OAuth app with Team Chat scopes. Zoom access tokens expire after 1 hour. Refresh tokens expire after 90 days, and Zoom requires using the latest refresh token on each refresh. PKCE is disabled for this wrapper because the current Zoom app/authorize flow is rejecting the code_challenge_method during connection setup. Zoom must have the exact MindCloud redirect URI allowlisted: https://api.mindcloud.co/v1/oauth/zoomTeamChat/callback . Redirect URI matching is exact, including case.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://zoom.us/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://zoom.us/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `team_chat:read:list_user_channels team_chat:read:channel team_chat:write:channel team_chat:read:list_members team_chat:write:members team_chat:read:list_messages team_chat:read:user_message team_chat:write:message team_chat:update:user_message team_chat:update:message_emoji team_chat:write:message_files team_chat:read:list_sessions team_chat:update:favorite_channel_or_contact team_chat:read:list_contacts team_chat:read:contact team_chat:write:contact_information team_chat:read:mention_group team_chat:write:mention_group team_chat:read:emoji team_chat:read:list_reminders team_chat:write:reminder team_chat:update:reminder team_chat:delete:reminder team_chat:read:shared_space team_chat:write:shared_space`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://zoom.us/oauth/token.

[Official authentication documentation](https://developers.zoom.us/docs/integrations/oauth/)

## API conventions

The next-page cursor is read from `next_page_token`.

## Pagination

Use `page_size` in the query string to set the page size (default 30). Use `next_page_token` in the query string as the pagination cursor.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Channel Members To A Mention Group](actions/add-channel-members-to-a-mention-group.md) | `POST /chat/channels/:channelId/mention_group/:mentionGroupId/members` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/) |
| [Create Channel](actions/create-channel.md) | `POST /chat/users/:userId/channels` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/createChannel) |
| [Create Channel Mention Group](actions/create-channel-mention-group.md) | `POST /chat/channels/:channelId/mention_group` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/) |
| [Create Reminder Message](actions/create-reminder-message.md) | `POST /chat/messages/:messageId/reminder` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/createReminderForMessage) |
| [Create Shared Space](actions/create-shared-space.md) | `POST /chat/spaces` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/createSpace) |
| [Delete Message](actions/delete-message.md) | `DELETE /chat/users/:userId/messages/:messageId` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/deleteChatMessage) |
| [Get Channel](actions/get-channel.md) | `GET /chat/users/:userId/channels/:channelId` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/getChannel) |
| [Get Message](actions/get-message.md) | `GET /chat/users/:userId/messages/:messageId` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/getChatMessage) |
| [Get Shared Space](actions/get-shared-space.md) | `GET /chat/spaces/:spaceId` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/getASharedSpace) |
| [Get User's Contact Details](actions/get-users-contact-details.md) | `GET /chat/users/me/contacts/:identifier` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/) |
| [Invite Channel Members](actions/invite-channel-members.md) | `POST /chat/users/:userId/channels/:channelId/members` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/inviteChannelMembers) |
| [Join Channel](actions/join-channel.md) | `POST /chat/channels/:channelId/members/me` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/joinChannel) |
| [Leave Channel](actions/leave-channel.md) | `DELETE /chat/channels/:channelId/members/me` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/leaveChannel) |
| [List Account's Public Channels](actions/list-accounts-public-channels.md) | `GET /chat/channels` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/getAccountChannels) |
| [List Channel Activity Logs](actions/list-channel-activity-logs.md) | `GET /chat/channels/:channelId/activities` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/listChannelActivityLogs) |
| [List Channel Administrators](actions/list-channel-administrators.md) | `GET /chat/users/:userId/channels/:channelId/admins` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/listChannelAdministrators) |
| [List Channel Members](actions/list-channel-members.md) | `GET /chat/users/:userId/channels/:channelId/members` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/listChannelMembers) |
| [List Channel Mention Groups](actions/list-channel-mention-groups.md) | `GET /chat/channels/:channelId/mention_group` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/) |
| [List Members Of A Mention Group](actions/list-members-of-a-mention-group.md) | `GET /chat/channels/:channelId/mention_group/:mentionGroupId/members` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/) |
| [List Reminders](actions/list-reminders.md) | `GET /chat/reminder` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/) |
| [List Shared Space Channels](actions/list-shared-space-channels.md) | `GET /chat/spaces/:spaceId/channels` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/listSharedSpaceChannels) |
| [List Shared Spaces](actions/list-shared-spaces.md) | `GET /chat/spaces` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/listSharedSpaces) |
| [List User's Channels](actions/list-user-channels.md) | `GET /chat/users/:userId/channels` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/getChannels) |
| [List User's Chat Messages](actions/list-users-chat-messages.md) | `GET /chat/users/:userId/messages` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/getChatMessages) |
| [List User's Chat Sessions](actions/list-users-chat-sessions.md) | `GET /chat/users/:userId/sessions` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/getChatSessions) |
| [List User's Contacts](actions/list-users-contacts.md) | `GET /chat/users/me/contacts` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/getUserContacts) |
| [Mark Message Read Or Unread](actions/mark-message-read-or-unread.md) | `PATCH /chat/users/:userId/messages/:messageId/status` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/markMessage) |
| [React To Chat Message](actions/react-to-chat-message.md) | `PATCH /chat/users/:userId/messages/:messageId/emoji_reactions` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/reactMessage) |
| [Retrieve Thread](actions/retrieve-thread.md) | `GET /chat/users/:userId/messages/:messageId/thread` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/retrieveThread) |
| [Search Company Contacts](actions/search-company-contacts.md) | `GET /contacts` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/searchCompanyContacts) |
| [Search User's Or Account's Channels](actions/search-users-or-accounts-channels.md) | `POST /chat/channels/search` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/searchChannels) |
| [Send Chat File](actions/send-chat-file.md) | `POST https://file.zoom.us/v2/chat/users/:userId/messages/files` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/sendChatFile) |
| [Send Chat Message](actions/send-chat-message.md) | `POST /chat/users/:userId/messages` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/sendaChatMessage) |
| [Send New Contact Invitation](actions/send-new-contact-invitation.md) | `POST /chat/users/:userId/invitations` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/sendNewContactInvitation) |
| [Star Or Unstar Channel Or Contact User](actions/star-or-unstar-channel-or-contact-user.md) | `PATCH /chat/users/:userId/events` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/starUnstarChannelContact) |
| [Update Channel](actions/update-channel.md) | `PATCH /chat/users/:userId/channels/:channelId` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/updateChannel) |
| [Update Channel Mention Group Information](actions/update-channel-mention-group-information.md) | `PATCH /chat/channels/:channelId/mention_group/:mentionGroupId` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/) |
| [Update Message](actions/update-message.md) | `PUT /chat/users/:userId/messages/:messageId` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/editMessage) |
| [Update Retention Policy Of A Channel](actions/update-retention-policy-of-a-channel.md) | `PATCH /chat/channels/:channelId/retention` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/updateChannelRetention) |
| [Upload Chat File](actions/upload-chat-file.md) | `POST https://file.zoom.us/v2/chat/users/:userId/files` | [docs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/uploadAChatFile) |
