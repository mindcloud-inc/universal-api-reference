# <img src="https://images.mindcloud.co/apps/icons/microsoft-office-teams-logo-512px_1776190929973.png" alt="Microsoft Teams logo" width="28" height="28"> Microsoft Teams: Universal API

Access Microsoft Teams collaboration data and actions through Microsoft Graph, including teams, channels, chats, messages, tabs, files folders, and installed apps. This app uses delegated Microsoft Entra OAuth2 for work or school accounts.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/microsoftTeams/latest
- **Category:** Communication / Team Messaging
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.microsoft.com/microsoft-teams
- **Vendor API docs:** https://learn.microsoft.com/en-us/graph/api/resources/teams-api-overview?view=graph-rest-1.0

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Joined Teams](actions/list-joined-teams.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/list-joined-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [List Channel Tabs](actions/list-channel-tabs.md) | GET | Retrieves channel tabs from Microsoft Teams. |
| [List Team Installed Apps](actions/list-team-installed-apps.md) | GET | Retrieves installed apps for a Microsoft Teams team. |

### Channels

| Action | Method | Description |
| --- | --- | --- |
| [Create Channel](actions/create-channel.md) | POST | Creates a new channel in Microsoft Teams. |
| [Get Channel](actions/get-channel.md) | GET | Retrieves a channel from Microsoft Teams. |
| [Get Team Primary Channel](actions/get-team-primary-channel.md) | GET | Retrieves a team's primary channel from Microsoft Teams. |
| [List All Team Channels](actions/list-all-team-channels.md) | GET | Retrieves all team channels from Microsoft Teams. |
| [List Team Channels](actions/list-team-channels.md) | GET | Retrieves team channels from Microsoft Teams. |
| [Update Channel](actions/update-channel.md) | PUT | Updates an existing channel in Microsoft Teams. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat](actions/create-chat.md) | POST | Creates a new chat in Microsoft Teams. |
| [Get Chat](actions/get-chat.md) | GET | Retrieves a chat from Microsoft Teams. |
| [List Chats](actions/list-chats.md) | GET | Retrieves chats from Microsoft Teams. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel Files Folder](actions/get-channel-files-folder.md) | GET | Retrieves a channel's files folder from Microsoft Teams. |

### Memberships

| Action | Method | Description |
| --- | --- | --- |
| [List Channel Members](actions/list-channel-members.md) | GET | Retrieves channel members from Microsoft Teams. |
| [List Chat Members](actions/list-chat-members.md) | GET | Retrieves chat members from Microsoft Teams. |
| [List Team Members](actions/list-team-members.md) | GET | Retrieves team members from Microsoft Teams. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [List Channel Message Replies](actions/list-channel-message-replies.md) | GET | Retrieves replies to a Microsoft Teams channel message. |
| [List Channel Messages](actions/list-channel-messages.md) | GET | Retrieves channel messages from Microsoft Teams. |
| [List Chat Messages](actions/list-chat-messages.md) | GET | Retrieves chat messages from Microsoft Teams. |
| [Reply To Channel Message](actions/reply-to-channel-message.md) | POST | Creates a reply to a Microsoft Teams channel message. |
| [Send Channel Message](actions/send-channel-message.md) | POST | Creates a new channel message in Microsoft Teams. |
| [Send Chat Message](actions/send-chat-message.md) | POST | Creates a new chat message in Microsoft Teams. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [Get Team](actions/get-team.md) | GET | Retrieves a team from Microsoft Teams. |
| [List Joined Teams](actions/list-joined-teams.md) | GET | Retrieves teams you've joined in Microsoft Teams. |

