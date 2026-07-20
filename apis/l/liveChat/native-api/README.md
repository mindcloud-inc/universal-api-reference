# LiveChat: Native API Reference

A consolidated summary of LiveChat's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://platform.text.com/docs/messaging/agent-chat-api/
- **API base URL:** `https://api.livechatinc.com/v3.6/agent/action`

## Authentication

### Personal Access Token

Connect LiveChat with your account ID and Personal Access Token.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://platform.text.com/docs/authorization/agent-authorization/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `chatsSummary`. The next-page cursor is read from `nextPageId`.

## Pagination

Use `limit` in the request body to set the page size (default 10; accepted range 1–100). Use `page_id` in the request body as the pagination cursor.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add User To Chat](actions/add-user-to-chat.md) | `POST /add_user_to_chat` | [docs](https://platform.text.com/docs/messaging/agent-chat-api#add-user-to-chat) |
| [Deactivate Chat](actions/deactivate-chat.md) | `POST /deactivate_chat` | [docs](https://platform.text.com/docs/messaging/agent-chat-api#deactivate-chat) |
| [Follow Chat](actions/follow-chat.md) | `POST /follow_chat` | [docs](https://platform.text.com/docs/messaging/agent-chat-api#follow-chat) |
| [Get Chat](actions/get-chat.md) | `POST /get_chat` | [docs](https://platform.text.com/docs/messaging/agent-chat-api#get-chat) |
| [Get Customer](actions/get-customer.md) | `POST /get_customer` | [docs](https://platform.text.com/docs/messaging/agent-chat-api#get-customer) |
| [List Agents For Transfer](actions/list-agents-for-transfer.md) | `POST /list_agents_for_transfer` | [docs](https://platform.text.com/docs/messaging/agent-chat-api#list-agents-for-transfer) |
| [List Archives](actions/list-archives.md) | `POST /list_archives` | [docs](https://platform.text.com/docs/messaging/agent-chat-api#list-archives) |
| [List Chats](actions/list-chats.md) | `POST /list_chats` | [docs](https://platform.text.com/docs/messaging/agent-chat-api#list-chats) |
| [List Routing Statuses](actions/list-routing-statuses.md) | `POST /list_routing_statuses` | [docs](https://platform.text.com/docs/messaging/agent-chat-api#list-routing-statuses) |
| [List Threads](actions/list-threads.md) | `POST /list_threads` | [docs](https://platform.text.com/docs/messaging/agent-chat-api#list-threads) |
| [Mark Events As Seen](actions/mark-events-as-seen.md) | `POST /mark_events_as_seen` | [docs](https://platform.text.com/docs/messaging/agent-chat-api#mark-events-as-seen) |
| [Remove User From Chat](actions/remove-user-from-chat.md) | `POST /remove_user_from_chat` | [docs](https://platform.text.com/docs/messaging/agent-chat-api#remove-user-from-chat) |
| [Resume Chat](actions/resume-chat.md) | `POST /resume_chat` | [docs](https://platform.text.com/docs/messaging/agent-chat-api#resume-chat) |
| [Send Event](actions/send-event.md) | `POST /send_event` | [docs](https://platform.text.com/docs/messaging/agent-chat-api#send-event) |
| [Send Rich Message Postback](actions/send-rich-message-postback.md) | `POST /send_rich_message_postback` | [docs](https://platform.text.com/docs/messaging/agent-chat-api#send-rich-message-postback) |
| [Set Routing Status](actions/set-routing-status.md) | `POST /set_routing_status` | [docs](https://platform.text.com/docs/messaging/agent-chat-api#set-routing-status) |
| [Start Chat](actions/start-chat.md) | `POST /start_chat` | [docs](https://platform.text.com/docs/messaging/agent-chat-api#start-chat) |
| [Tag Thread](actions/tag-thread.md) | `POST /tag_thread` | [docs](https://platform.text.com/docs/messaging/agent-chat-api#tag-thread) |
| [Transfer Chat](actions/transfer-chat.md) | `POST /transfer_chat` | [docs](https://platform.text.com/docs/messaging/agent-chat-api#transfer-chat) |
| [Unfollow Chat](actions/unfollow-chat.md) | `POST /unfollow_chat` | [docs](https://platform.text.com/docs/messaging/agent-chat-api#unfollow-chat) |
| [Untag Thread](actions/untag-thread.md) | `POST /untag_thread` | [docs](https://platform.text.com/docs/messaging/agent-chat-api#untag-thread) |
| [Update Chat Properties](actions/update-chat-properties.md) | `POST /update_chat_properties` | [docs](https://platform.text.com/docs/messaging/agent-chat-api#update-chat-properties) |
| [Update Customer](actions/update-customer.md) | `POST /update_customer` | [docs](https://platform.text.com/docs/messaging/agent-chat-api#update-customer) |
| [Upload File](actions/upload-file.md) | `POST /upload_file` | [docs](https://platform.text.com/docs/messaging/agent-chat-api#upload-file) |
