# Sendbird: Native API Reference

A consolidated summary of Sendbird's API configuration and 48 documented operations, with links to official documentation.

- **Official docs:** https://docs.sendbird.com/docs/chat/platform-api/v3/prepare-to-use-api
- **API base URL:** `https://api-{applicationId}.sendbird.com/v3`

## Authentication

### Sendbird API Credentials

Authenticate Sendbird Chat Platform API requests with an application ID and API token.

### Credentials

- **Application ID:** `applicationId` · required · Your Sendbird application ID from Settings > Application > General.
- **API Token:** `apiKey` · required · Your Sendbird master or secondary API token.

Send these headers with each API request:

```http
Api-Token: <apiKey>
```

[Official authentication documentation](https://docs.sendbird.com/docs/chat/platform-api/v3/prepare-to-use-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf8` |

Responses from this API use JSON. Response data is read from `users`. The next-page cursor is read from `next`.

## Endpoints (48 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Accept Group Channel Invitation](actions/accept-group-channel-invitation.md) | `PUT /group_channels/:channelUrl/accept` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/managing-members/accept-an-invitation) |
| [Check Group Channel Member](actions/check-group-channel-member.md) | `GET /group_channels/:channelUrl/members/:userId` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/managing-members/check-if-user-is-a-member) |
| [Create Group Channel](actions/create-group-channel.md) | `POST /group_channels` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/creating-a-channel/create-a-group-channel) |
| [Create Group Channel Custom Type](actions/create-group-channel-custom-type.md) | `POST /group_channels/custom_types` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/managing-application-settings/create-a-custom-channel-type) |
| [Create Group Channel Metacounters](actions/create-group-channel-metacounters.md) | `POST /group_channels/:channelUrl/metacounter` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/managing-channel-metacounter/create-channel-metacounters) |
| [Create Group Channel Metadata](actions/create-group-channel-metadata.md) | `POST /group_channels/:channelUrl/metadata` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/managing-channel-metadata/create-channel-metadata) |
| [Create Open Channel](actions/create-open-channel.md) | `POST /open_channels` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/creating-a-channel/create-an-open-channel) |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/user/managing-users/create-a-user) |
| [Decline Group Channel Invitation](actions/decline-group-channel-invitation.md) | `PUT /group_channels/:channelUrl/decline` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/managing-members/decline-an-invitation) |
| [Delete Group Channel](actions/delete-group-channel.md) | `DELETE /group_channels/:channelUrl` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/managing-a-channel/delete-a-group-channel) |
| [Delete Group Channel Custom Type](actions/delete-group-channel-custom-type.md) | `DELETE /group_channels/custom_types/:customType` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/managing-application-settings/delete-a-custom-channel-type) |
| [Delete Group Channel Metacounters](actions/delete-group-channel-metacounters.md) | `DELETE /group_channels/:channelUrl/metacounter` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/managing-channel-metacounter/delete-channel-metacounters) |
| [Delete Group Channel Metadata](actions/delete-group-channel-metadata.md) | `DELETE /group_channels/:channelUrl/metadata` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/managing-channel-metadata/delete-channel-metadata) |
| [Delete Open Channel](actions/delete-open-channel.md) | `DELETE /open_channels/:channelUrl` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/managing-a-channel/delete-an-open-channel) |
| [Delete User](actions/delete-user.md) | `DELETE /users/:userId` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/user/managing-users/delete-a-user) |
| [Get Announcement](actions/get-announcement.md) | `GET /announcements/:uniqueId` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/message/announcements/announcement-overview) |
| [Get Bot](actions/get-bot.md) | `GET /bots/:botUserid` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/bot/bot-overview) |
| [Get Channel Invitation Preference](actions/get-channel-invitation-preference.md) | `GET /users/:userId/channel_invitation_preference` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/managing-a-channel/get-channel-invitation-preference) |
| [Get Group Channel](actions/get-group-channel.md) | `GET /group_channels/:channelUrl` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/channel-overview) |
| [Get Group Channel Custom Type](actions/get-group-channel-custom-type.md) | `GET /group_channels/custom_types/:customType` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/managing-application-settings/get-channel-settings-for-a-custom-channel-type) |
| [Get Open Channel](actions/get-open-channel.md) | `GET /open_channels/:channelUrl` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/channel-overview) |
| [Get Poll](actions/get-poll.md) | `GET /polls/:pollId` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/message/polls/polls-overview) |
| [Get User](actions/get-user.md) | `GET /users/:userId` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/user/listing-users/get-a-user) |
| [Hide Group Channel](actions/hide-group-channel.md) | `PUT /group_channels/:channelUrl/hide` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/managing-a-channel/hide-a-channel) |
| [Invite Group Channel Members](actions/invite-group-channel-members.md) | `POST /group_channels/:channelUrl/invite` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/managing-members/invite-as-members) |
| [Join Group Channel](actions/join-group-channel.md) | `PUT /group_channels/:channelUrl/join` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/joining-and-leaving-a-channel/join-a-channel) |
| [Leave Group Channel](actions/leave-group-channel.md) | `PUT /group_channels/:channelUrl/leave` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/joining-and-leaving-a-channel/leave-a-channel) |
| [List Announcements](actions/list-announcements.md) | `GET /announcements` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/message/announcements/list-announcements) |
| [List Bots](actions/list-bots.md) | `GET /bots` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/bot/listing-bots/list-bots) |
| [List Data Exports](actions/list-data-exports.md) | `GET /export/:dataType` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/data-export/data-export-overview) |
| [List Group Channel Custom Types](actions/list-group-channel-custom-types.md) | `GET /group_channels/custom_types` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/managing-application-settings/list-custom-channel-types) |
| [List Group Channel Members](actions/list-group-channel-members.md) | `GET /group_channels/:channelUrl/members` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/managing-members/list-members-of-a-group-channel) |
| [List Group Channels](actions/list-group-channels.md) | `GET /group_channels` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/listing-channels-in-an-application/list-group-channels) |
| [List Group Channels By User](actions/list-group-channels-by-user.md) | `GET /users/:userId/my_group_channels` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/user/managing-joined-group-channels/list-group-channels-by-user) |
| [List Open Channel Participants](actions/list-open-channel-participants.md) | `GET /open_channels/:channelUrl/participants` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/listing-participants/list-participants-of-an-open-channel) |
| [List Open Channels](actions/list-open-channels.md) | `GET /open_channels` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/channel-overview) |
| [List Polls](actions/list-polls.md) | `GET /polls` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/message/polls/list-polls) |
| [List Reports](actions/list-reports.md) | `GET /report` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/report/listing-reports/list-reports) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/user/listing-users/list-users) |
| [Reset Group Channel User History](actions/reset-group-channel-user-history.md) | `PUT /group_channels/:channelUrl/reset_user_history` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/managing-a-channel/reset-chat-history) |
| [Unhide Group Channel](actions/unhide-group-channel.md) | `DELETE /group_channels/:channelUrl/hide` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/managing-a-channel/unhide-a-channel) |
| [Update Channel Invitation Preference](actions/update-channel-invitation-preference.md) | `PUT /users/:userId/channel_invitation_preference` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/managing-a-channel/update-channel-invitation-preference) |
| [Update Group Channel](actions/update-group-channel.md) | `PUT /group_channels/:channelUrl` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/managing-a-channel/update-a-group-channel) |
| [Update Group Channel Custom Type](actions/update-group-channel-custom-type.md) | `PUT /group_channels/custom_types/:customType` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/managing-application-settings/update-channel-settings-for-a-custom-channel-type) |
| [Update Group Channel Metacounters](actions/update-group-channel-metacounters.md) | `PUT /group_channels/:channelUrl/metacounter` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/managing-channel-metacounter/update-channel-metacounters) |
| [Update Group Channel Metadata](actions/update-group-channel-metadata.md) | `PUT /group_channels/:channelUrl/metadata` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/managing-channel-metadata/update-channel-metadata) |
| [Update Open Channel](actions/update-open-channel.md) | `PUT /open_channels/:channelUrl` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/managing-a-channel/update-an-open-channel) |
| [Update User](actions/update-user.md) | `PUT /users/:userId` | [docs](https://docs.sendbird.com/docs/chat/platform-api/v3/user/managing-users/update-a-user) |
