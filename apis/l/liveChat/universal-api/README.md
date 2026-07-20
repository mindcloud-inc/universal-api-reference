# <img src="https://images.mindcloud.co/apps/icons/live-chat_1773324719076.png" alt="LiveChat logo" width="28" height="28"> LiveChat: Universal API

Manage LiveChat chats, customers, routing, and messaging operations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/liveChat/latest
- **Category:** Support / Ticketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.livechat.com/
- **Vendor API docs:** https://platform.text.com/docs/messaging/agent-chat-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Chats](actions/list-chats.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/list-chats?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [List Agents For Transfer](actions/list-agents-for-transfer.md) | GET | Retrieves agents available for chat transfer in LiveChat. |

### Archive

| Action | Method | Description |
| --- | --- | --- |
| [List Archives](actions/list-archives.md) | GET | Retrieves archived chats and thread events from LiveChat. |

### Chat

| Action | Method | Description |
| --- | --- | --- |
| [Deactivate Chat](actions/deactivate-chat.md) | PUT | Updates a chat by deactivating it in LiveChat. |
| [Follow Chat](actions/follow-chat.md) | PUT | Updates a chat by following it in LiveChat. |
| [Get Chat](actions/get-chat.md) | GET | Retrieves a chat with thread details from LiveChat. |
| [List Chats](actions/list-chats.md) | GET | Retrieves accessible chat summaries from LiveChat. |
| [Resume Chat](actions/resume-chat.md) | POST | Restarts an archived chat in LiveChat. |
| [Start Chat](actions/start-chat.md) | POST | Creates a new chat in LiveChat. |
| [Transfer Chat](actions/transfer-chat.md) | PUT | Updates a chat by transferring it in LiveChat. |
| [Unfollow Chat](actions/unfollow-chat.md) | PUT | Updates a chat by unfollowing it in LiveChat. |
| [Update Chat Properties](actions/update-chat-properties.md) | PUT | Updates existing chat properties in LiveChat. |

### Chat User

| Action | Method | Description |
| --- | --- | --- |
| [Add User To Chat](actions/add-user-to-chat.md) | PUT | Updates a chat by adding a user in LiveChat. |
| [Remove User From Chat](actions/remove-user-from-chat.md) | PUT | Updates a chat by removing a user in LiveChat. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | GET | Retrieves detailed customer information from LiveChat. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in LiveChat. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Mark Events As Seen](actions/mark-events-as-seen.md) | PUT | Updates chat events as seen in LiveChat. |
| [Send Event](actions/send-event.md) | POST | Sends a new event in LiveChat. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Upload File](actions/upload-file.md) | POST | Creates a temporary file upload in LiveChat. |

### Rich Message Postback

| Action | Method | Description |
| --- | --- | --- |
| [Send Rich Message Postback](actions/send-rich-message-postback.md) | POST | Sends a rich message postback in LiveChat. |

### Routing Status

| Action | Method | Description |
| --- | --- | --- |
| [List Routing Statuses](actions/list-routing-statuses.md) | GET | Retrieves agent routing statuses from LiveChat. |
| [Set Routing Status](actions/set-routing-status.md) | PUT | Updates an agent routing status in LiveChat. |

### Thread

| Action | Method | Description |
| --- | --- | --- |
| [List Threads](actions/list-threads.md) | GET | Retrieves accessible chat threads from LiveChat. |
| [Tag Thread](actions/tag-thread.md) | PUT | Updates a thread by tagging it in LiveChat. |
| [Untag Thread](actions/untag-thread.md) | PUT | Updates a thread by untagging it in LiveChat. |

