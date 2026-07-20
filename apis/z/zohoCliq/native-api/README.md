# Zoho Cliq: Native API Reference

A consolidated summary of Zoho Cliq's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.zoho.com/cliq/help/restapi/v2/
- **OpenAPI specification:** https://oas-download-files-development.zohostratus.com/cliq/cliq-openapi-all.zip
- **API base URL:** `https://cliq.zoho.com/api/v2`

## Authentication

### OAuth2

OAuth 2.0 authorization code flow for Zoho Cliq.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://accounts.zoho.com/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `ZohoCliq.Channels.CREATE,ZohoCliq.Channels.READ,ZohoCliq.Channels.UPDATE,ZohoCliq.Chats.READ,ZohoCliq.Messages.READ,ZohoCliq.Messages.UPDATE,ZohoCliq.Messages.DELETE,ZohoCliq.Profile.READ,ZohoCliq.Reminders.ALL,ZohoCliq.Webhooks.CREATE`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://accounts.zoho.com/oauth/v2/token.

[Official authentication documentation](https://www.zoho.com/cliq/help/restapi/v2/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Channel Members](actions/add-channel-members.md) | `POST /channels/:channelId/members` | [docs](https://www.zoho.com/cliq/help/restapi/v2/#Channels_Add_Members) |
| [Complete Reminder](actions/complete-reminder.md) | `PUT /reminders/:reminderId/complete` | [docs](https://www.zoho.com/cliq/help/restapi/v2/#mark_reminder_complete) |
| [Create Channel](actions/create-channel.md) | `POST /channels` | [docs](https://www.zoho.com/cliq/help/restapi/v2/#Channels_Create_a_channel) |
| [Delete Chat Message](actions/delete-chat-message.md) | `DELETE /chats/:chatId/messages/:messageId` | [docs](https://www.zoho.com/cliq/help/restapi/v2/#Delete_Message) |
| [Get Thread Main Message](actions/get-thread-main-message.md) | `GET /threads/:threadChatId/messages/main` | [docs](https://www.zoho.com/cliq/help/restapi/v2/#get-main-message) |
| [Join Channel](actions/join-channel.md) | `POST /channels/:channelId/join` | [docs](https://www.zoho.com/cliq/help/restapi/v2/#Channels_Join_a_Channel) |
| [Leave Channel](actions/leave-channel.md) | `POST /channels/:channelId/leave` | [docs](https://www.zoho.com/cliq/help/restapi/v2/#Channels_Leave_a_Channel) |
| [List Channel Members](actions/list-channel-members.md) | `GET /channels/:channelId/members` | [docs](https://www.zoho.com/cliq/help/restapi/v2/#Channels_Get_Members) |
| [List Channel Threads](actions/list-channel-threads.md) | `GET /channels/:channelId/threads` | [docs](https://www.zoho.com/cliq/help/restapi/v2/#get-thread) |
| [List Channels](actions/list-channels.md) | `GET /channels` | [docs](https://www.zoho.com/cliq/help/restapi/v2/#Channels_List_all_channel) |
| [List Chat Members](actions/list-chat-members.md) | `GET /chats/:chatId/members` | [docs](https://www.zoho.com/cliq/help/restapi/v2/#retrieve-members) |
| [List Chat Messages](actions/list-chat-messages.md) | `GET /chats/:chatId/messages` | [docs](https://www.zoho.com/cliq/help/restapi/v2/#Get_Messages) |
| [List Direct Chats](actions/list-direct-chats.md) | `GET /chats` | [docs](https://www.zoho.com/cliq/help/restapi/v2/#retrieve-chats) |
| [List Reminders](actions/list-reminders.md) | `GET /reminders` | [docs](https://www.zoho.com/cliq/help/restapi/v2/#list_all_reminders) |
| [Remove Channel Members](actions/remove-channel-members.md) | `DELETE /channels/:channelId/members` | [docs](https://www.zoho.com/cliq/help/restapi/v2/#Channels_Delete_Members) |
| [Retrieve Channel](actions/retrieve-channel.md) | `GET /channels/:channelId` | [docs](https://www.zoho.com/cliq/help/restapi/v2/#Channels_Retrieve_a_channel) |
| [Retrieve Chat Message](actions/retrieve-chat-message.md) | `GET /chats/:chatId/messages/:messageId` | [docs](https://www.zoho.com/cliq/help/restapi/v2/#Retrieve_Message) |
| [Retrieve Current Status](actions/retrieve-current-status.md) | `GET /statuses/current` | [docs](https://www.zoho.com/cliq/help/restapi/v2/#retrieve-current-status) |
| [Retrieve Reminder](actions/retrieve-reminder.md) | `GET /reminders/:reminderId` | [docs](https://www.zoho.com/cliq/help/restapi/v2/#get_reminder) |
| [Send Chat Message](actions/send-chat-message.md) | `POST /chats/:chatId/message` | [docs](https://www.zoho.com/cliq/help/restapi/v2/#Post_Message_Chat) |
| [Set Self Reminder](actions/set-self-reminder.md) | `POST /reminders` | [docs](https://www.zoho.com/cliq/help/restapi/v2/#create_reminder_self) |
| [Update Channel](actions/update-channel.md) | `PUT /channels/:channelId` | [docs](https://www.zoho.com/cliq/help/restapi/v2/#Channels_Update_a_channel) |
| [Update Chat Message](actions/update-chat-message.md) | `PUT /chats/:chatId/messages/:messageId` | [docs](https://www.zoho.com/cliq/help/restapi/v2/#Edit_Message) |
| [Update Reminder](actions/update-reminder.md) | `PUT /reminders/:reminderId` | [docs](https://www.zoho.com/cliq/help/restapi/v2/#update_reminder) |
