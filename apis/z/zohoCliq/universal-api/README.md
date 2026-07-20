# <img src="https://images.mindcloud.co/apps/icons/zoho-cliq_1773408506928.png" alt="Zoho Cliq logo" width="28" height="28"> Zoho Cliq: Universal API

Chat in channels, collaborate in threads, manage reminders, and track status updates in Zoho Cliq.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoCliq/latest
- **Category:** Communication / Team Messaging
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cliq.zoho.com/
- **Vendor API docs:** https://www.zoho.com/cliq/help/restapi/v2/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Current Status](actions/retrieve-current-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/retrieve-current-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Create Channel](actions/create-channel.md) | POST | Creates a new channel in Zoho Cliq. |
| [Join Channel](actions/join-channel.md) | PUT | Joins a channel in Zoho Cliq. |
| [Leave Channel](actions/leave-channel.md) | PUT | Leaves a channel in Zoho Cliq. |
| [List Channels](actions/list-channels.md) | GET | Retrieves Zoho Cliq channels by filters. |
| [Retrieve Channel](actions/retrieve-channel.md) | GET | Retrieves a channel from Zoho Cliq by ID. |
| [Update Channel](actions/update-channel.md) | PUT | Updates an existing channel in Zoho Cliq. |

### Channel Member

| Action | Method | Description |
| --- | --- | --- |
| [Add Channel Members](actions/add-channel-members.md) | PUT | Adds members to a Zoho Cliq channel. |
| [List Channel Members](actions/list-channel-members.md) | GET | Retrieves members of a Zoho Cliq channel. |
| [Remove Channel Members](actions/remove-channel-members.md) | DELETE | Removes members from a Zoho Cliq channel. |

### Chat

| Action | Method | Description |
| --- | --- | --- |
| [List Direct Chats](actions/list-direct-chats.md) | GET | Retrieves direct chats from Zoho Cliq. |

### Chat Member

| Action | Method | Description |
| --- | --- | --- |
| [List Chat Members](actions/list-chat-members.md) | GET | Retrieves members of a Zoho Cliq chat. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Delete Chat Message](actions/delete-chat-message.md) | DELETE | Deletes an existing chat message from Zoho Cliq. |
| [List Chat Messages](actions/list-chat-messages.md) | GET | Retrieves messages from a Zoho Cliq chat. |
| [Retrieve Chat Message](actions/retrieve-chat-message.md) | GET | Retrieves a chat message from Zoho Cliq by ID. |
| [Send Chat Message](actions/send-chat-message.md) | POST | Creates a new chat message in Zoho Cliq. |
| [Update Chat Message](actions/update-chat-message.md) | PUT | Updates an existing chat message in Zoho Cliq. |

### Reminder

| Action | Method | Description |
| --- | --- | --- |
| [Complete Reminder](actions/complete-reminder.md) | PUT | Marks a Zoho Cliq reminder as complete. |
| [List Reminders](actions/list-reminders.md) | GET | Retrieves all reminders from Zoho Cliq. |
| [Retrieve Reminder](actions/retrieve-reminder.md) | GET | Retrieves a reminder from Zoho Cliq by ID. |
| [Set Self Reminder](actions/set-self-reminder.md) | POST | Creates a self reminder in Zoho Cliq. |
| [Update Reminder](actions/update-reminder.md) | PUT | Updates an existing reminder in Zoho Cliq. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Current Status](actions/retrieve-current-status.md) | GET | Retrieves the current user status from Zoho Cliq. |

### Thread

| Action | Method | Description |
| --- | --- | --- |
| [Get Thread Main Message](actions/get-thread-main-message.md) | GET | Retrieves the main message of a Zoho Cliq thread. |
| [List Channel Threads](actions/list-channel-threads.md) | GET | Retrieves threads from a Zoho Cliq channel. |

