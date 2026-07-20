# <img src="https://images.mindcloud.co/apps/icons/element_1776361246544.png" alt="Element logo" width="28" height="28"> Element: Universal API

Element is a Matrix client for secure team communication and collaboration. This draft wraps the Matrix Client-Server API for authenticated account and messaging operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/element/latest
- **Category:** Communication / Team Messaging
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://element.io/
- **Vendor API docs:** https://docs.element.io/latest/element-support/advanced-administration/getting-started-using-the-client-server-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/element/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [Get Capabilities](actions/get-capabilities.md) | GET | Retrieves supported capabilities from Element. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Create Room](actions/create-room.md) | POST | Creates a room in Element. |
| [Forget Room](actions/forget-room.md) | DELETE | Forgets a room in Element for the current user. |
| [Get Joined Rooms](actions/get-joined-rooms.md) | GET | Retrieves joined rooms from Element. |
| [Get Room State](actions/get-room-state.md) | GET | Retrieves a room's state from Element. |
| [Join Room](actions/join-room.md) | POST | Joins a room in Element by ID or alias. |
| [Leave Room](actions/leave-room.md) | PUT | Leaves a room in Element for the current user. |

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [Get Device](actions/get-device.md) | GET | Retrieves a device from Element. |
| [Get Devices](actions/get-devices.md) | GET | Retrieves devices from Element. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Get Room Event](actions/get-room-event.md) | GET | Retrieves a room event from Element. |
| [Send Room Message](actions/send-room-message.md) | POST | Creates a message in an Element room. |
| [Set Typing Indicator](actions/set-typing-indicator.md) | PUT | Updates a room's typing indicator in Element. |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [Get Pushers](actions/get-pushers.md) | GET | Retrieves push notification pushers from Element. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Element. |
| [Get Joined Members](actions/get-joined-members.md) | GET | Retrieves joined room members from Element. |
| [Get Presence Status](actions/get-presence-status.md) | GET | Retrieves a user's presence status from Element. |
| [Get Profile](actions/get-profile.md) | GET | Retrieves a user's profile from Element. |
| [Search User Directory](actions/search-user-directory.md) | GET | Finds users in Element by search term. |
| [Set Display Name](actions/set-display-name.md) | PUT | Updates a user's display name in Element. |
| [Set Presence Status](actions/set-presence-status.md) | PUT | Updates a user's presence status in Element. |

