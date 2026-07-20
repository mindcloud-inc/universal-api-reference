# <img src="https://images.mindcloud.co/apps/icons/instabot_1777039599285.png" alt="Instabot logo" width="28" height="28"> Instabot: Universal API

Build chatbots that answer questions, capture leads, and book meetings

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/instabot/latest
- **Category:** Communication / Team Messaging
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.instabot.io
- **Vendor API docs:** https://docs.instabot.io/docs/serverapi

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Application Info](actions/get-application-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instabot/latest/actions/get-application-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Get Application Info](actions/get-application-info.md) | GET | Retrieves application details from Instabot. |

### Bot

| Action | Method | Description |
| --- | --- | --- |
| [List Bots](actions/list-bots.md) | GET | Retrieves bots from Instabot. |

### Bot Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Bot Common Summary Of Reply](actions/get-bot-common-summary-of-reply.md) | GET | Retrieves a bot reply summary from Instabot. |
| [Get Bot Itemized Summary Of Reply](actions/get-bot-itemized-summary-of-reply.md) | GET | Retrieves an itemized bot reply summary from Instabot. |

### Chat

| Action | Method | Description |
| --- | --- | --- |
| [Search Chats](actions/search-chats.md) | GET | Finds chats in Instabot by search filters. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves conversations from Instabot. |

### Display Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Display Settings](actions/get-display-settings.md) | GET | Retrieves display settings from Instabot. |

### Live Chat Status Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Live Chat Status Counts](actions/get-live-chat-status-counts.md) | GET | Retrieves live chat status counts from Instabot. |

### Message Template

| Action | Method | Description |
| --- | --- | --- |
| [List Message Templates](actions/list-message-templates.md) | GET | Retrieves message templates from Instabot. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from Instabot. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in Instabot. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes an existing user from Instabot. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Instabot. |
| [List Recently Updated Users](actions/list-recently-updated-users.md) | GET | Finds users in Instabot by update time. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Instabot. |
| [Restore User](actions/restore-user.md) | PUT | Restores a deleted user in Instabot. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Instabot. |

