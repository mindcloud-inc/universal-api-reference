# Element: Native API Reference

A consolidated summary of Element's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.element.io/latest/element-support/advanced-administration/getting-started-using-the-client-server-api/
- **API base URL:** `{homeserverUrl}`

## Authentication

### Access Token

Matrix Client-Server API bearer token for an Element account. This auth also requires the account's homeserver URL as connection metadata.

### Credentials

- **API Key:** `apiKey` · required
- **Homeserver URL:** `homeserverUrl` · required · Full Matrix homeserver client base URL for this account, for example https://matrix-client.matrix.org.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.element.io/latest/element-support/advanced-administration/getting-started-using-the-client-server-api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Room](actions/create-room.md) | `POST /_matrix/client/v3/createRoom` | [docs](https://spec.matrix.org/latest/client-server-api/#post_matrixclientv3createroom) |
| [Forget Room](actions/forget-room.md) | `POST /_matrix/client/v3/rooms/:roomId/forget` | [docs](https://spec.matrix.org/latest/client-server-api/#post_matrixclientv3roomsroomidforget) |
| [Get Capabilities](actions/get-capabilities.md) | `GET /_matrix/client/v3/capabilities` | [docs](https://spec.matrix.org/latest/client-server-api/#get_matrixclientv3capabilities) |
| [Get Current User](actions/get-current-user.md) | `GET /_matrix/client/v3/account/whoami` | [docs](https://spec.matrix.org/latest/client-server-api/#get_matrixclientv3accountwhoami) |
| [Get Device](actions/get-device.md) | `GET /_matrix/client/v3/devices/:deviceId` | [docs](https://spec.matrix.org/latest/client-server-api/#get_matrixclientv3devicesdeviceid) |
| [Get Devices](actions/get-devices.md) | `GET /_matrix/client/v3/devices` | [docs](https://spec.matrix.org/latest/client-server-api/#get_matrixclientv3devices) |
| [Get Joined Members](actions/get-joined-members.md) | `GET /_matrix/client/v3/rooms/:roomId/joined_members` | [docs](https://spec.matrix.org/latest/client-server-api/#get_matrixclientv3roomsroomidjoined_members) |
| [Get Joined Rooms](actions/get-joined-rooms.md) | `GET /_matrix/client/v3/joined_rooms` | [docs](https://spec.matrix.org/latest/client-server-api/#get_matrixclientv3joined_rooms) |
| [Get Presence Status](actions/get-presence-status.md) | `GET /_matrix/client/v3/presence/:userId/status` | [docs](https://spec.matrix.org/latest/client-server-api/#get_matrixclientv3presenceuseridstatus) |
| [Get Profile](actions/get-profile.md) | `GET /_matrix/client/v3/profile/:userId` | [docs](https://spec.matrix.org/latest/client-server-api/#get_matrixclientv3profileuserid) |
| [Get Pushers](actions/get-pushers.md) | `GET /_matrix/client/v3/pushers` | [docs](https://spec.matrix.org/latest/client-server-api/#get_matrixclientv3pushers) |
| [Get Room Event](actions/get-room-event.md) | `GET /_matrix/client/v3/rooms/:roomId/event/:eventId` | [docs](https://spec.matrix.org/latest/client-server-api/#get_matrixclientv3roomsroomideventeventid) |
| [Get Room State](actions/get-room-state.md) | `GET /_matrix/client/v3/rooms/:roomId/state` | [docs](https://spec.matrix.org/latest/client-server-api/#get_matrixclientv3roomsroomidstate) |
| [Join Room](actions/join-room.md) | `POST /_matrix/client/v3/join/:roomIdOrAlias` | [docs](https://spec.matrix.org/latest/client-server-api/#post_matrixclientv3joinroomidoralias) |
| [Leave Room](actions/leave-room.md) | `POST /_matrix/client/v3/rooms/:roomId/leave` | [docs](https://spec.matrix.org/latest/client-server-api/#post_matrixclientv3roomsroomidleave) |
| [Search User Directory](actions/search-user-directory.md) | `POST /_matrix/client/v3/user_directory/search` | [docs](https://spec.matrix.org/latest/client-server-api/#post_matrixclientv3user_directorysearch) |
| [Send Room Message](actions/send-room-message.md) | `PUT /_matrix/client/v3/rooms/:roomId/send/m.room.message/:txnId` | [docs](https://spec.matrix.org/latest/client-server-api/#put_matrixclientv3roomsroomidsendeventtypetxnid) |
| [Set Display Name](actions/set-display-name.md) | `PUT /_matrix/client/v3/profile/:userId/displayname` | [docs](https://spec.matrix.org/latest/client-server-api/#put_matrixclientv3profileuseriddisplayname) |
| [Set Presence Status](actions/set-presence-status.md) | `PUT /_matrix/client/v3/presence/:userId/status` | [docs](https://spec.matrix.org/latest/client-server-api/#put_matrixclientv3presenceuseridstatus) |
| [Set Typing Indicator](actions/set-typing-indicator.md) | `PUT /_matrix/client/v3/rooms/:roomId/typing/:userId` | [docs](https://spec.matrix.org/latest/client-server-api/#put_matrixclientv3roomsroomidtypinguserid) |
