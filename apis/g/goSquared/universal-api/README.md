# <img src="https://images.mindcloud.co/apps/icons/go-squared_1774557543174.png" alt="GoSquared logo" width="28" height="28"> GoSquared: Universal API

GoSquared: Track visitors, analyze traffic, and manage live chats

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/goSquared/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.gosquared.com/
- **Vendor API docs:** https://www.gosquared.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sites](actions/list-sites.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/list-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Blocked Bots Setting

| Action | Method | Description |
| --- | --- | --- |
| [Get Blocked Bots Setting](actions/get-blocked-bots-setting.md) | GET | Retrieves the blocked bots setting from GoSquared. |

### Blocked Ip

| Action | Method | Description |
| --- | --- | --- |
| [List Blocked IPs](actions/list-blocked-ips.md) | GET | Retrieves blocked IP addresses from GoSquared. |

### Blocked Visitor

| Action | Method | Description |
| --- | --- | --- |
| [List Blocked Visitors](actions/list-blocked-visitors.md) | GET | Retrieves blocked visitors for a GoSquared site. |

### Chat

| Action | Method | Description |
| --- | --- | --- |
| [List Active Chats](actions/list-active-chats.md) | GET | Retrieves active chats for a GoSquared site. |
| [List Archived Chats](actions/list-archived-chats.md) | GET | Retrieves archived chats for a GoSquared site. |

### Device

| Action | Method | Description |
| --- | --- | --- |
| [List Devices](actions/list-devices.md) | GET | Retrieves visitor devices tracked in GoSquared. |

### Event Type

| Action | Method | Description |
| --- | --- | --- |
| [List Event Types](actions/list-event-types.md) | GET | Retrieves person event types from GoSquared. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Get Person](actions/get-person.md) | GET | Retrieves a person from GoSquared by ID. |
| [List Smart Group People](actions/list-smart-group-people.md) | GET | Retrieves people from a GoSquared smart group. |
| [Search People](actions/search-people.md) | GET | Finds people in GoSquared by search query. |

### Person Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Person Feed](actions/get-person-feed.md) | GET | Retrieves a person's feed events from GoSquared. |

### Property Type

| Action | Method | Description |
| --- | --- | --- |
| [List Property Types](actions/list-property-types.md) | GET | Retrieves person property types from GoSquared. |

### Shared User

| Action | Method | Description |
| --- | --- | --- |
| [List Shared Users](actions/list-shared-users.md) | GET | Retrieves account shared users from GoSquared. |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [List Sites](actions/list-sites.md) | GET | Retrieves sites from the connected GoSquared account. |

### Smart Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Smart Group](actions/get-smart-group.md) | GET | Retrieves a smart group from GoSquared by ID. |
| [List Smart Groups](actions/list-smart-groups.md) | GET | Retrieves people smart groups from GoSquared. |

### Tagged Visitor

| Action | Method | Description |
| --- | --- | --- |
| [List Tagged Visitors](actions/list-tagged-visitors.md) | GET | Retrieves tagged visitors for a GoSquared site. |

### Trigger Type

| Action | Method | Description |
| --- | --- | --- |
| [List Trigger Types](actions/list-trigger-types.md) | GET | Retrieves account trigger types from GoSquared. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves account webhooks configured in GoSquared. |

