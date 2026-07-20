# <img src="https://images.mindcloud.co/apps/icons/images-1_1773871978406.png" alt="Zoom Team Chat logo" width="28" height="28"> Zoom Team Chat: Universal API

Use Zoom Team Chat to list channels, contacts, sessions, messages, reminders, and shared spaces, and to send and manage Team Chat content through Zoom's API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zoomTeamChat/latest
- **Category:** Communication / Team Messaging
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://zoom.us
- **Vendor API docs:** https://developers.zoom.us/docs/api/rest/reference/chat/methods/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List User's Channels](actions/list-user-channels.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/list-user-channels?connectionId=$CONNECTION_ID&limit=25&offset=0&userId=me" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Create Channel](actions/create-channel.md) | POST |  |
| [Get Channel](actions/get-channel.md) | GET |  |
| [List Account's Public Channels](actions/list-accounts-public-channels.md) | GET |  |
| [List Shared Space Channels](actions/list-shared-space-channels.md) | GET |  |
| [List User's Channels](actions/list-user-channels.md) | GET |  |
| [Search User's Or Account's Channels](actions/search-users-or-accounts-channels.md) | GET |  |
| [Update Channel](actions/update-channel.md) | PUT |  |

### Channel Activity Log

| Action | Method | Description |
| --- | --- | --- |
| [List Channel Activity Logs](actions/list-channel-activity-logs.md) | GET |  |

### Channel Administrator

| Action | Method | Description |
| --- | --- | --- |
| [List Channel Administrators](actions/list-channel-administrators.md) | GET |  |

### Channel Member

| Action | Method | Description |
| --- | --- | --- |
| [Invite Channel Members](actions/invite-channel-members.md) | POST |  |
| [List Channel Members](actions/list-channel-members.md) | GET |  |

### Channel Membership

| Action | Method | Description |
| --- | --- | --- |
| [Join Channel](actions/join-channel.md) | POST |  |
| [Leave Channel](actions/leave-channel.md) | DELETE |  |

### Channel Retention Policy

| Action | Method | Description |
| --- | --- | --- |
| [Update Retention Policy Of A Channel](actions/update-retention-policy-of-a-channel.md) | PUT |  |

### Chat Session

| Action | Method | Description |
| --- | --- | --- |
| [List User's Chat Sessions](actions/list-users-chat-sessions.md) | GET |  |
| [Star Or Unstar Channel Or Contact User](actions/star-or-unstar-channel-or-contact-user.md) | PUT |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get User's Contact Details](actions/get-users-contact-details.md) | GET |  |
| [List User's Contacts](actions/list-users-contacts.md) | GET |  |
| [Search Company Contacts](actions/search-company-contacts.md) | GET |  |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Send Chat File](actions/send-chat-file.md) | POST |  |
| [Upload Chat File](actions/upload-chat-file.md) | POST |  |

### Invitation

| Action | Method | Description |
| --- | --- | --- |
| [Send New Contact Invitation](actions/send-new-contact-invitation.md) | POST |  |

### Mention Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Channel Mention Group](actions/create-channel-mention-group.md) | POST |  |
| [List Channel Mention Groups](actions/list-channel-mention-groups.md) | GET |  |
| [Update Channel Mention Group Information](actions/update-channel-mention-group-information.md) | PUT |  |

### Mention Group Member

| Action | Method | Description |
| --- | --- | --- |
| [Add Channel Members To A Mention Group](actions/add-channel-members-to-a-mention-group.md) | PUT |  |
| [List Members Of A Mention Group](actions/list-members-of-a-mention-group.md) | GET |  |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Delete Message](actions/delete-message.md) | DELETE |  |
| [Get Message](actions/get-message.md) | GET |  |
| [List User's Chat Messages](actions/list-users-chat-messages.md) | GET |  |
| [Send Chat Message](actions/send-chat-message.md) | POST |  |
| [Update Message](actions/update-message.md) | PUT |  |

### Message Reaction

| Action | Method | Description |
| --- | --- | --- |
| [React To Chat Message](actions/react-to-chat-message.md) | PUT |  |

### Message Status

| Action | Method | Description |
| --- | --- | --- |
| [Mark Message Read Or Unread](actions/mark-message-read-or-unread.md) | PUT |  |

### Reminder

| Action | Method | Description |
| --- | --- | --- |
| [Create Reminder Message](actions/create-reminder-message.md) | POST |  |
| [List Reminders](actions/list-reminders.md) | GET |  |

### Shared Space

| Action | Method | Description |
| --- | --- | --- |
| [Create Shared Space](actions/create-shared-space.md) | POST |  |
| [Get Shared Space](actions/get-shared-space.md) | GET |  |
| [List Shared Spaces](actions/list-shared-spaces.md) | GET |  |

### Thread Message

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Thread](actions/retrieve-thread.md) | GET |  |

