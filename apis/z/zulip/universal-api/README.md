# <img src="https://images.mindcloud.co/apps/icons/zulip_1774547203884.png" alt="Zulip logo" width="28" height="28"> Zulip: Universal API

Zulip: Send messages and manage channels, users, and events

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zulip/latest
- **Category:** Communication / Team Messaging
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://zulip.com
- **Vendor API docs:** https://zulip.com/api/rest

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Own User](actions/get-own-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zulip/latest/actions/get-own-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel by ID](actions/get-channel-by-id.md) | GET | Retrieves a Zulip channel by ID. |
| [Get Channel ID](actions/get-channel-id.md) | GET | Finds a Zulip channel ID by name. |
| [List Channels](actions/list-channels.md) | GET | Retrieves all channels available in Zulip. |
| [List Topics in a Channel](actions/list-topics-in-a-channel.md) | GET | Retrieves topics in a specific Zulip channel. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Delete Event Queue](actions/delete-event-queue.md) | DELETE | Deletes an existing Zulip event queue. |
| [List Events](actions/list-events.md) | GET | Retrieves events from a Zulip event queue. |
| [Register Event Queue](actions/register-event-queue.md) | POST | Registers a real-time event queue in Zulip. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Add Emoji Reaction](actions/add-emoji-reaction.md) | PUT | Adds an emoji reaction to a Zulip message. |
| [Delete Message](actions/delete-message.md) | DELETE | Deletes an existing message from Zulip. |
| [Edit Message](actions/edit-message.md) | PUT | Updates an existing message in Zulip. |
| [Fetch Single Message](actions/fetch-single-message.md) | GET | Retrieves a single Zulip message by ID. |
| [List Messages](actions/list-messages.md) | GET | Retrieves messages from Zulip using specified filters. |
| [Remove Emoji Reaction](actions/remove-emoji-reaction.md) | DELETE | Removes an emoji reaction from a Zulip message. |
| [Render Message](actions/render-message.md) | GET | Renders Zulip message content into HTML. |
| [Send Message](actions/send-message.md) | POST | Creates a new message in Zulip. |

### Server Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Server Settings](actions/get-server-settings.md) | GET | Retrieves current server settings from Zulip. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscription Status](actions/get-subscription-status.md) | GET | Retrieves a user's subscription status for a Zulip channel. |
| [List Channel Subscribers](actions/list-channel-subscribers.md) | GET | Retrieves subscribers for a specific Zulip channel. |
| [List Subscribed Channels](actions/list-subscribed-channels.md) | GET | Retrieves subscribed channels for the requesting Zulip user. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Own User](actions/get-own-user.md) | GET | Retrieves the requesting user's Zulip account details. |
| [Get User](actions/get-user.md) | GET | Retrieves a specific Zulip user by ID. |
| [Get User by Email](actions/get-user-by-email.md) | GET | Retrieves a specific Zulip user by email address. |
| [Get User Presence](actions/get-user-presence.md) | GET | Retrieves a Zulip user's presence information. |
| [Get User Status](actions/get-user-status.md) | GET | Retrieves a Zulip user's current status details. |
| [List Users](actions/list-users.md) | GET | Retrieves Zulip users from the organization directory. |

