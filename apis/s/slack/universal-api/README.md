# <img src="https://images.mindcloud.co/apps/icons/image-2824-vectorized_1777321878663.png" alt="Slack logo" width="28" height="28"> Slack: Universal API

Chat in channels, share knowledge, automate workflows, and join huddles.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/slack/latest
- **Category:** Communication / Team Messaging
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://slack.com/
- **Vendor API docs:** https://docs.slack.dev/reference/methods/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/slack/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Create Channel](actions/create-channel.md) | POST | Creates a new channel in Slack. |
| [Get Channel Information](actions/get-channel-information.md) | GET | Retrieves conversation details from a Slack workspace. |
| [Join Channel](actions/join-channel.md) | PUT | Joins an existing conversation in Slack. |
| [Leave Channel](actions/leave-channel.md) | DELETE | Leaves an existing conversation in Slack. |
| [List Channels](actions/list-channels.md) | GET | Retrieves channels from a Slack workspace. |
| [Set Channel Topic](actions/set-channel-topic.md) | PUT | Updates a conversation topic in Slack. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Open Conversation](actions/open-conversation.md) | POST | Opens or resumes a direct conversation in Slack. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE | Deletes an existing file from Slack. |
| [Get File Information](actions/get-file-information.md) | GET | Retrieves file details from a Slack workspace. |
| [List Files](actions/list-files.md) | GET | Retrieves files from a Slack workspace. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Delete Message](actions/delete-message.md) | DELETE | Deletes an existing message from Slack. |
| [List Channel Messages](actions/list-channel-messages.md) | GET | Retrieves channel messages and events from Slack. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Delete Scheduled Message](actions/delete-scheduled-message.md) | DELETE | Deletes a scheduled message from Slack. |
| [List Message Replies](actions/list-message-replies.md) | GET | Retrieves replies from a Slack conversation thread. |
| [List Scheduled Messages](actions/list-scheduled-messages.md) | GET | Retrieves scheduled messages from a Slack workspace. |
| [Schedule Message](actions/schedule-message.md) | POST | Creates a scheduled message in Slack. |
| [Send Channel Message](actions/send-channel-message.md) | POST | Creates a new message in a Slack channel. |
| [Send User Message](actions/send-user-message.md) | POST | Creates a new direct message in Slack. |
| [Update Message](actions/update-message.md) | PUT | Updates an existing message in Slack. |

### Reaction

| Action | Method | Description |
| --- | --- | --- |
| [Add Reaction](actions/add-reaction.md) | POST | Adds a reaction to an item in Slack. |
| [List Message Reactions](actions/list-message-reactions.md) | GET | Retrieves reactions for an item in Slack. |
| [List User Reactions](actions/list-user-reactions.md) | GET | Retrieves reactions made by a Slack user. |
| [Remove Reaction](actions/remove-reaction.md) | DELETE | Removes a reaction from an item in Slack. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Set Presence](actions/set-status.md) | PUT | Updates the current user's Slack presence. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Invite User to Channel](actions/invite-user-to-channel.md) | POST | Invites users to a Slack channel. |
| [Search Channels and Users](actions/search-channels-and-users.md) | GET | Finds Slack channels and users by search query. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User Information](actions/get-user-information.md) | GET | Retrieves user details from a Slack workspace. |
| [Kick User From Channel](actions/kick-user-from-channel.md) | DELETE | Removes a user from a Slack conversation. |
| [List Channel Members](actions/list-channel-members.md) | GET | Retrieves conversation members from a Slack workspace. |
| [List Users](actions/list-users.md) | GET | Retrieves users from a Slack workspace. |
| [Search User By Email](actions/search-user-by-email.md) | GET | Finds a Slack user by email address. |

