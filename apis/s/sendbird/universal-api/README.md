# <img src="https://images.mindcloud.co/apps/icons/sendbird-icon-512_1776185965578.png" alt="Sendbird logo" width="28" height="28"> Sendbird: Universal API

Sendbird Chat Platform API for managing users, channels, messages, moderation, application settings, webhooks, reports, bots, exports, and analytics.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sendbird/latest
- **Category:** Communication / Team Messaging
- **Actions:** 48
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sendbird.com
- **Vendor API docs:** https://docs.sendbird.com/docs/chat/platform-api/v3/prepare-to-use-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (48)

### Announcements

| Action | Method | Description |
| --- | --- | --- |
| [Get Announcement](actions/get-announcement.md) | GET |  |
| [List Announcements](actions/list-announcements.md) | GET |  |

### Channels

| Action | Method | Description |
| --- | --- | --- |
| [Accept Group Channel Invitation](actions/accept-group-channel-invitation.md) | PUT |  |
| [Create Group Channel](actions/create-group-channel.md) | POST |  |
| [Create Group Channel Metacounters](actions/create-group-channel-metacounters.md) | POST |  |
| [Create Group Channel Metadata](actions/create-group-channel-metadata.md) | POST |  |
| [Create Open Channel](actions/create-open-channel.md) | POST |  |
| [Decline Group Channel Invitation](actions/decline-group-channel-invitation.md) | PUT |  |
| [Delete Group Channel](actions/delete-group-channel.md) | DELETE |  |
| [Delete Group Channel Metacounters](actions/delete-group-channel-metacounters.md) | DELETE |  |
| [Delete Group Channel Metadata](actions/delete-group-channel-metadata.md) | DELETE |  |
| [Delete Open Channel](actions/delete-open-channel.md) | DELETE |  |
| [Get Group Channel](actions/get-group-channel.md) | GET |  |
| [Get Open Channel](actions/get-open-channel.md) | GET |  |
| [Hide Group Channel](actions/hide-group-channel.md) | PUT |  |
| [Invite Group Channel Members](actions/invite-group-channel-members.md) | POST |  |
| [Join Group Channel](actions/join-group-channel.md) | PUT |  |
| [Leave Group Channel](actions/leave-group-channel.md) | PUT |  |
| [List Group Channels](actions/list-group-channels.md) | GET |  |
| [List Group Channels By User](actions/list-group-channels-by-user.md) | GET |  |
| [List Open Channels](actions/list-open-channels.md) | GET |  |
| [Reset Group Channel User History](actions/reset-group-channel-user-history.md) | PUT |  |
| [Unhide Group Channel](actions/unhide-group-channel.md) | DELETE |  |
| [Update Group Channel](actions/update-group-channel.md) | PUT |  |
| [Update Group Channel Metacounters](actions/update-group-channel-metacounters.md) | PUT |  |
| [Update Group Channel Metadata](actions/update-group-channel-metadata.md) | PUT |  |
| [Update Open Channel](actions/update-open-channel.md) | PUT |  |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [List Reports](actions/list-reports.md) | GET |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Group Channel Custom Type](actions/create-group-channel-custom-type.md) | POST |  |
| [Delete Group Channel Custom Type](actions/delete-group-channel-custom-type.md) | DELETE |  |
| [Get Bot](actions/get-bot.md) | GET |  |
| [Get Channel Invitation Preference](actions/get-channel-invitation-preference.md) | GET |  |
| [Get Group Channel Custom Type](actions/get-group-channel-custom-type.md) | GET |  |
| [Get Poll](actions/get-poll.md) | GET |  |
| [List Bots](actions/list-bots.md) | GET |  |
| [List Data Exports](actions/list-data-exports.md) | GET |  |
| [List Group Channel Custom Types](actions/list-group-channel-custom-types.md) | GET |  |
| [List Polls](actions/list-polls.md) | GET |  |
| [Update Channel Invitation Preference](actions/update-channel-invitation-preference.md) | PUT |  |
| [Update Group Channel Custom Type](actions/update-group-channel-custom-type.md) | PUT |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Check Group Channel Member](actions/check-group-channel-member.md) | GET |  |
| [Create User](actions/create-user.md) | POST |  |
| [Delete User](actions/delete-user.md) | DELETE |  |
| [Get User](actions/get-user.md) | GET |  |
| [List Group Channel Members](actions/list-group-channel-members.md) | GET |  |
| [List Open Channel Participants](actions/list-open-channel-participants.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |
| [Update User](actions/update-user.md) | PUT |  |

